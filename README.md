import React from 'react';
import { 
  Mail, MapPin, Briefcase, GraduationCap, Cpu, 
  Globe, ExternalLink, Award, Zap, Sparkles, 
  Linkedin, Facebook, ChevronRight, Phone,
  Layers, Terminal, CheckCircle
} from 'lucide-react';

/**
 * ==========================================
 * 1. CONFIGURATION / DATA CENTER
 * ==========================================
 * Edit your data here to update the website.
 */
const DATA = {
  profile: {
    name: "Tikso SAYALUB",
    title: "Ecotourism Specialist & Digital Transformation Advocate",
    location: "Vientiane Capital, Laos",
    email: "tiksobig@gmail.com",
    phone: "+856 20 7739 6741",
    bio: "A highly motivated final-year Ecotourism student at the National University of Laos. With a professional background in international coordination (UN agencies) and high-tech production (Japan), I specialize in leveraging AI and digital innovations to drive environmental sustainability and community empowerment."
  },
  experience: [
    {
      id: 1,
      company: "Digital Data Divide (DDD) Vientiane",
      role: "Associate",
      period: "May 2025 - August 2025",
      description: "Optimized digital data management workflows and increased operational efficiency through the strategic integration of AI tools like Gemini and ChatGPT in a corporate environment."
    },
    {
      id: 2,
      company: "Eco Green Agriculture (Helvetas & Zero Waste Laos)",
      role: "Project Facilitator & Team Member",
      period: "June 2025 - September 2025",
      description: "Co-implemented a community sustainability project focused on MJU organic fertilizer and soil analysis (pH testing) for local farmers, funded by international NGOs."
    },
    {
      id: 3,
      company: "FAO (United Nations Agency)",
      role: "Online Volunteer (Logistics & Coordination)",
      period: "2025",
      description: "Coordinated logistics for the Lao National Youth Forum 2025 and collaborated with South Korean teams to develop Climate-Smart Agriculture (CSA) interactive tools."
    },
    {
      id: 4,
      company: "Yukiguni Maitake Co., Ltd (Japan)",
      role: "Production Intern",
      period: "2024 - 2025",
      description: "Successfully completed a 6-month professional internship in Niigata, Japan, mastering high-tech agricultural production systems and strict international quality control standards."
    }
  ],
  skills: {
    computer: [
      { name: "Microsoft Office Suite", level: "Very Good", percentage: 90, color: "bg-indigo-600" },
      { name: "AI Tools (Gemini, ChatGPT)", level: "Good", percentage: 85, color: "bg-purple-600" },
      { name: "QGIS & Mapping", level: "Good", percentage: 70, color: "bg-emerald-600" },
      { name: "Google Workspace & Mail", level: "Good", percentage: 80, color: "bg-blue-600" },
      { name: "Canva & Digital Assets", level: "Good", percentage: 75, color: "bg-rose-600" }
    ],
    languages: [
      { name: "English", speaking: "Good", writing: "Fair", listening: "Good", reading: "Good", badge: "Professional" },
      { name: "Japanese", speaking: "Good", writing: "Fail", listening: "Good", reading: "Fair", badge: "N3 Level" },
      { name: "Lao", speaking: "Excellence", writing: "Excellence", listening: "Excellence", reading: "Excellence", badge: "Native" },
      { name: "Khumu", speaking: "Native", writing: "-", listening: "Native", reading: "-", badge: "Native Oral" }
    ]
  },
  education: [
    {
      school: "National University of Laos (NUOL)",
      degree: "Bachelor of Science in Forestry (Ecotourism)",
      period: "2022 - Present"
    }
  ]
};

/**
 * ==========================================
 * 2. SUB-COMPONENTS
 * ==========================================
 */

const SkillBar = ({ name, level, percentage, color }) => (
  <div className="mb-6 group">
    <div className="flex justify-between items-end mb-2">
      <span className="text-sm font-bold text-slate-700 tracking-tight group-hover:text-indigo-600 transition-colors">{name}</span>
      <span className="text-[10px] font-black uppercase text-slate-400 bg-slate-50 px-2 py-0.5 rounded border border-slate-100">{level}</span>
    </div>
    <div className="w-full bg-slate-100 rounded-full h-2 overflow-hidden border border-slate-50">
      <div 
        className={`${color} h-full transition-all duration-1000 ease-out`}
        style={{ width: `${percentage}%` }}
      ></div>
    </div>
  </div>
);

const ExperienceItem = ({ exp }) => (
  <div className="relative pl-12 pb-12 last:pb-0 group">
    <div className="absolute left-0 top-0 bottom-0 w-px bg-slate-100 group-last:bg-transparent"></div>
    <div className="absolute left-[-8px] top-0 w-4 h-4 rounded-full bg-white border-4 border-indigo-600 shadow-sm transition-all group-hover:scale-125"></div>
    <div className="bg-white p-8 rounded-[2rem] border border-slate-100 shadow-sm hover:shadow-xl hover:shadow-indigo-50/50 transition-all hover:-translate-y-1">
      <div className="flex flex-col md:flex-row md:justify-between items-start md:items-center gap-4 mb-4">
        <div>
          <h3 className="text-xl font-black text-slate-900 uppercase tracking-tight">{exp.company}</h3>
          <p className="text-indigo-600 font-bold text-xs uppercase tracking-widest">{exp.role}</p>
        </div>
        <span className="text-[10px] font-black bg-slate-50 text-slate-400 px-3 py-1.5 rounded-full border border-slate-100 uppercase">{exp.period}</span>
      </div>
      <p className="text-slate-500 text-sm leading-relaxed italic border-l-2 border-indigo-50 pl-4">
        {exp.description}
      </p>
    </div>
  </div>
);

/**
 * ==========================================
 * 3. MAIN APPLICATION COMPONENT
 * ==========================================
 */

const App = () => {
  return (
    <div className="min-h-screen bg-[#FCFDFF] text-slate-900 font-sans selection:bg-indigo-100 selection:text-indigo-900">
      
      {/* --- HERO / HEADER --- */}
      <header className="relative bg-white pt-32 pb-20 md:pt-48 md:pb-32 overflow-hidden">
        <div className="absolute top-0 right-0 w-1/3 h-full bg-indigo-50/50 -skew-x-12 translate-x-1/4 -z-0"></div>
        <div className="max-w-6xl mx-auto px-6 relative z-10">
          <div className="flex flex-col md:flex-row items-center gap-12 md:gap-20">
            <div className="relative">
              <div className="w-48 h-48 md:w-72 md:h-72 bg-slate-900 rounded-[3rem] flex items-center justify-center text-white text-7xl font-black shadow-2xl relative rotate-3 hover:rotate-0 transition-transform duration-500">
                {DATA.profile.name.charAt(0)}
              </div>
              <div className="absolute -bottom-6 -right-6 bg-white p-5 rounded-3xl shadow-xl border border-slate-50 animate-bounce">
                <Sparkles className="text-indigo-600" size={32} />
              </div>
            </div>
            
            <div className="text-center md:text-left flex-1">
              <div className="inline-flex items-center gap-2 px-4 py-1.5 bg-indigo-50 text-indigo-700 rounded-full text-[10px] font-black uppercase tracking-[0.2em] mb-6 shadow-sm shadow-indigo-100">
                <Zap size={14} fill="currentColor" /> Ready for Impact
              </div>
              <h1 className="text-5xl md:text-8xl font-black text-slate-900 tracking-tighter leading-none mb-4 uppercase">
                {DATA.profile.name}
              </h1>
              <p className="text-xl md:text-2xl text-slate-500 font-medium mb-10">
                {DATA.profile.title}
              </p>
              
              <div className="flex flex-wrap justify-center md:justify-start gap-6 text-[10px] font-black text-slate-400 uppercase tracking-[0.2em]">
                <span className="flex items-center gap-2"><MapPin size={16} className="text-indigo-600" /> {DATA.profile.location}</span>
                <span className="flex items-center gap-2"><Mail size={16} className="text-indigo-600" /> {DATA.profile.email}</span>
              </div>
            </div>
          </div>
        </div>
      </header>

      {/* --- ABOUT SECTION --- */}
      <section className="py-24 bg-slate-900 text-white">
        <div className="max-w-4xl mx-auto px-6 text-center">
          <h2 className="text-[10px] font-black uppercase tracking-[0.5em] text-indigo-400 mb-12">Professional Mission</h2>
          <p className="text-2xl md:text-4xl font-light leading-tight text-slate-300 italic">
            "{DATA.profile.bio}"
          </p>
        </div>
      </section>

      {/* --- MAIN CONTENT GRID --- */}
      <main className="max-w-6xl mx-auto px-6 py-32 space-y-40">
        
        {/* EXPERIENCE SECTION */}
        <section id="experience">
          <div className="flex items-center gap-4 mb-16">
            <div className="p-3 bg-indigo-600 text-white rounded-2xl shadow-lg shadow-indigo-100"><Briefcase size={24} /></div>
            <h2 className="text-3xl font-black uppercase tracking-tighter">Experience</h2>
          </div>
          <div className="max-w-4xl">
            {DATA.experience.map(exp => (
              <ExperienceItem key={exp.id} exp={exp} />
            ))}
          </div>
        </section>

        {/* SKILLS SECTION */}
        <section id="skills" className="grid grid-cols-1 lg:grid-cols-12 gap-20">
          {/* Digital Skills */}
          <div className="lg:col-span-5">
            <div className="flex items-center gap-4 mb-12">
              <div className="p-3 bg-indigo-600 text-white rounded-2xl shadow-lg shadow-indigo-100"><Cpu size={24} /></div>
              <h2 className="text-3xl font-black uppercase tracking-tighter">Tech Stack</h2>
            </div>
            <div className="bg-white p-10 rounded-[3rem] border border-slate-100 shadow-sm">
              {DATA.skills.computer.map((skill, i) => (
                <SkillBar key={i} {...skill} />
              ))}
            </div>
          </div>
          
          {/* Languages Matrix */}
          <div className="lg:col-span-7">
            <div className="flex items-center gap-4 mb-12">
              <div className="p-3 bg-indigo-600 text-white rounded-2xl shadow-lg shadow-indigo-100"><Globe size={24} /></div>
              <h2 className="text-3xl font-black uppercase tracking-tighter">Languages</h2>
            </div>
            <div className="bg-white rounded-[3rem] border border-slate-100 shadow-sm overflow-hidden">
              <div className="overflow-x-auto">
                <table className="w-full text-left">
                  <thead>
                    <tr className="bg-slate-50 border-b border-slate-100 text-[10px] font-black text-slate-400 uppercase tracking-[0.2em]">
                      <th className="px-8 py-6">Language</th>
                      <th className="px-4 py-6 text-center">Speak</th>
                      <th className="px-4 py-6 text-center">Write</th>
                      <th className="px-4 py-6 text-center">Listen</th>
                      <th className="px-4 py-6 text-center">Read</th>
                    </tr>
                  </thead>
                  <tbody className="divide-y divide-slate-50">
                    {DATA.skills.languages.map((lang, i) => (
                      <tr key={i} className="hover:bg-indigo-50/20 transition-colors">
                        <td className="px-8 py-6">
                          <span className="font-black text-slate-900 block">{lang.name}</span>
                          <span className="text-[9px] font-bold text-indigo-500 uppercase tracking-tighter">{lang.badge}</span>
                        </td>
                        <td className="px-4 py-6 text-[10px] text-slate-500 text-center font-bold uppercase">{lang.speaking}</td>
                        <td className="px-4 py-6 text-[10px] text-slate-500 text-center font-bold uppercase">{lang.writing}</td>
                        <td className="px-4 py-6 text-[10px] text-slate-500 text-center font-bold uppercase">{lang.listening}</td>
                        <td className="px-4 py-6 text-[10px] text-slate-500 text-center font-bold uppercase">{lang.reading}</td>
                      </tr>
                    ))}
                  </tbody>
                </table>
              </div>
              <div className="p-8 bg-amber-50/50 border-t border-amber-100 flex items-start gap-3">
                <Award size={18} className="text-amber-600 mt-0.5 shrink-0" />
                <p className="text-[10px] text-amber-800 italic leading-relaxed">
                  Note: Khumu is an oral-tradition language natively spoken in my community. It does not have a formal written system; hence proficiency is measured by verbal and auditory mastery.
                </p>
              </div>
            </div>
          </div>
        </section>

        {/* EDUCATION SECTION */}
        <section id="education">
          <div className="flex items-center gap-4 mb-16">
            <div className="p-3 bg-indigo-600 text-white rounded-2xl shadow-lg shadow-indigo-100"><GraduationCap size={24} /></div>
            <h2 className="text-3xl font-black uppercase tracking-tighter">Academic Background</h2>
          </div>
          <div className="grid md:grid-cols-2 gap-8">
            {DATA.education.map((edu, i) => (
              <div key={i} className="p-10 bg-white border border-slate-100 rounded-[2.5rem] shadow-sm flex items-center gap-6">
                <div className="w-16 h-16 bg-slate-100 rounded-2xl flex items-center justify-center text-slate-400">
                  <Layers size={32} />
                </div>
                <div>
                  <h3 className="font-black text-slate-900 uppercase tracking-tight">{edu.school}</h3>
                  <p className="text-indigo-600 font-bold text-sm">{edu.degree}</p>
                  <p className="text-[10px] font-black text-slate-300 uppercase tracking-widest mt-2">{edu.period}</p>
                </div>
              </div>
            ))}
          </div>
        </section>

      </main>

      {/* --- FOOTER / CONTACT --- */}
      <footer id="contact" className="bg-slate-950 text-white py-40 overflow-hidden relative">
        <div className="absolute top-0 right-0 w-1/2 h-full bg-white/5 -skew-x-12 translate-x-1/3"></div>
        <div className="max-w-6xl mx-auto px-6 relative z-10 text-center">
          <h2 className="text-5xl md:text-9xl font-black italic text-white/5 mb-24 tracking-tighter uppercase leading-none">Connect</h2>
          
          <div className="grid md:grid-cols-2 gap-8 max-w-4xl mx-auto mb-24 text-left">
            <div className="p-12 bg-white/5 rounded-[3.5rem] border border-white/10 group hover:border-indigo-500 transition-colors">
              <p className="text-[10px] font-black text-slate-500 uppercase tracking-[0.3em] mb-4">Official Inquiry</p>
              <a href={`mailto:${DATA.profile.email}`} className="text-xl md:text-2xl font-bold flex items-center justify-between group-hover:text-indigo-400 transition-colors">
                {DATA.profile.email} <ExternalLink size={20} />
              </a>
            </div>
            <div className="p-12 bg-white/5 rounded-[3.5rem] border border-white/10 group hover:border-indigo-500 transition-colors">
              <p className="text-[10px] font-black text-slate-500 uppercase tracking-[0.3em] mb-4">Direct Channel</p>
              <p className="text-xl md:text-2xl font-bold group-hover:text-indigo-400 transition-colors">
                {DATA.profile.phone}
              </p>
            </div>
          </div>

          <div className="flex justify-center gap-8 mb-20">
            <a href="#" className="p-5 bg-white/5 rounded-2xl hover:text-indigo-400 hover:bg-white/10 transition-all shadow-xl shadow-black/20"><Facebook /></a>
            <a href="#" className="p-5 bg-white/5 rounded-2xl hover:text-indigo-400 hover:bg-white/10 transition-all shadow-xl shadow-black/20"><Linkedin /></a>
          </div>
          
          <p className="text-slate-600 text-[10px] font-black uppercase tracking-[0.8em]">© 2026 TIKSO SAYALUB • DESIGNED FOR GLOBAL LEADERSHIP</p>
        </div>
      </footer>
    </div>
  );
};

export default App;
