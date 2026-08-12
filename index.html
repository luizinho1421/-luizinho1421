<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>LZK</title>
    <!-- Tailwind CSS 3.4 CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- React, ReactDOM, Babel -->
    <script src="https://unpkg.com/react@18/umd/react.production.min.js"></script>
    <script src="https://unpkg.com/react-dom@18/umd/react-dom.production.min.js"></script>
    <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
    <!-- Framer Motion -->
    <script src="https://unpkg.com/framer-motion@11.11.17/dist/framer-motion.js"></script>
    <!-- Hello Pangea DnD -->
    <script src="https://unpkg.com/@hello-pangea/dnd@16.6.0/dist/dnd.js"></script>
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&family=Space+Grotesk:wght@500;700&display=swap" rel="stylesheet">
    
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                        display: ['Space Grotesk', 'sans-serif'],
                    },
                }
            }
        }
    </script>
    <style>
        body {
            background-color: #0a0a0a;
            color: white;
            font-family: 'Inter', sans-serif;
            margin: 0;
            padding: 0;
        }
        /* Custom scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #0a0a0a;
        }
        ::-webkit-scrollbar-thumb {
            background: #333;
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #444;
        }
        /* Selection color */
        ::selection {
            background: rgba(239, 68, 68, 0.3);
        }
        #root {
            min-height: 100vh;
            display: flex;
            flex-direction: column;
        }
    </style>
</head>
<body>
    <div id="root"></div>

    <script type="text/babel">
        const { useState, useRef, useEffect } = React;
        
        // Safely access globals with fallbacks to standard HTML tags if libraries fail
        const Motion = window.Motion || {};
        const motion = Motion.motion || {
            div: 'div',
            h1: 'h1',
            p: 'p',
            button: 'button',
            span: 'span',
            section: 'section',
            main: 'main',
            footer: 'footer'
        };
        const AnimatePresence = Motion.AnimatePresence || (({children}) => children);
        
        const DnD = window.ReactBeautifulDnd || {};
        const DragDropContext = DnD.DragDropContext || (({children}) => <div>{children}</div>);
        const Droppable = DnD.Droppable || (({children}) => children({ 
            droppableProps: {}, 
            innerRef: () => {}, 
            placeholder: null 
        }));
        const Draggable = DnD.Draggable || (({children}) => children({ 
            draggableProps: {}, 
            dragHandleProps: {}, 
            innerRef: () => {} 
        }, {}));

        // Custom SVG Icons (Lucide replacements)
        const Icon = ({ children, size = 24, className = "", ...props }) => (
            <svg
                xmlns="http://www.w3.org/2000/svg"
                width={size}
                height={size}
                viewBox="0 0 24 24"
                fill="none"
                stroke="currentColor"
                strokeWidth="2"
                strokeLinecap="round"
                strokeLinejoin="round"
                className={className}
                {...props}
            >
                {children}
            </svg>
        );

        const Youtube = (props) => (
            <Icon {...props}><path d="M2.5 17a24.12 24.12 0 0 1 0-10 2 2 0 0 1 2-2h15a2 2 0 0 1 2 2 24.12 24.12 0 0 1 0 10 2 2 0 0 1-2 2h-15a2 2 0 0 1-2-2Z"/><path d="m10 15 5-3-5-3z"/></Icon>
        );
        const Instagram = (props) => (
            <Icon {...props}><rect width="20" height="20" x="2" y="2" rx="5" ry="5"/><path d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z"/><line x1="17.5" x2="17.51" y1="6.5" y2="6.5"/></Icon>
        );
        const Twitch = (props) => (
            <Icon {...props}><path d="M21 2H3v16h5v4l4-4h5l4-4V2zm-10 9V7m5 4V7"/></Icon>
        );
        const Send = (props) => (
            <Icon {...props}><line x1="22" x2="11" y1="2" y2="13"/><polygon points="22 2 15 22 11 13 2 9 22 2"/></Icon>
        );
        const Music2 = (props) => (
            <Icon {...props}><circle cx="8" cy="18" r="4"/><path d="M12 18V2l7 4"/></Icon>
        );
        const Gamepad2 = (props) => (
            <Icon {...props}><line x1="6" x2="10" y1="12" y2="12"/><line x1="8" x2="8" y1="10" y2="14"/><circle cx="15" cy="13" r="1"/><circle cx="18" cy="11" r="1"/><path d="M18 20a2 2 0 0 0 2-2V6a2 2 0 0 0-2-2H6a2 2 0 0 0-2 2v12a2 2 0 0 0 2 2Z"/></Icon>
        );
        const Mail = (props) => (
            <Icon {...props}><rect width="20" height="16" x="2" y="4" rx="2"/><path d="m22 7-8.97 5.7a1.94 1.94 0 0 1-2.06 0L2 7"/></Icon>
        );
        const ImageIcon = (props) => (
            <Icon {...props}><rect width="18" height="18" x="3" y="3" rx="2" ry="2"/><circle cx="9" cy="9" r="2"/><path d="m21 15-3.086-3.086a2 2 0 0 0-2.828 0L6 21"/></Icon>
        );
        const ExternalLink = (props) => (
            <Icon {...props}><path d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"/><polyline points="15 3 21 3 21 9"/><line x1="10" x2="21" y1="14" y2="3"/></Icon>
        );
        const Users = (props) => (
            <Icon {...props}><path d="M16 21v-2a4 4 0 0 0-4-4H6a4 4 0 0 0-4 4v2"/><circle cx="9" cy="7" r="4"/><path d="M22 21v-2a4 4 0 0 0-3-3.87"/><path d="M16 3.13a4 4 0 0 1 0 7.75"/></Icon>
        );
        const Settings = (props) => (
            <Icon {...props}><path d="M12.22 2h-.44a2 2 0 0 0-2 2v.18a2 2 0 0 1-1 1.73l-.43.25a2 2 0 0 1-2 0l-.15-.08a2 2 0 0 0-2.73.73l-.22.38a2 2 0 0 0 .73 2.73l.15.1a2 2 0 0 1 1 1.72v.51a2 2 0 0 1-1 1.74l-.15.09a2 2 0 0 0-.73 2.73l.22.38a2 2 0 0 0 2.73.73l.15-.08a2 2 0 0 1 2 0l.43.25a2 2 0 0 1 1 1.73V20a2 2 0 0 0 2 2h.44a2 2 0 0 0 2-2v-.18a2 2 0 0 1 1-1.73l.43-.25a2 2 0 0 1 2 0l.15.08a2 2 0 0 0 2.73-.73l.22-.38a2 2 0 0 0-.73-2.73l-.15-.1a2 2 0 0 1-1-1.72v-.51a2 2 0 0 1 1-1.74l.15-.09a2 2 0 0 0 .73-2.73l-.22-.38a2 2 0 0 0-2.73-.73l-.15.08a2 2 0 0 1-2 0l-.43-.25a2 2 0 0 1-1-1.73V4a2 2 0 0 0-2-2z"/><circle cx="12" cy="12" r="3"/></Icon>
        );
        const X = (props) => (
            <Icon {...props}><line x1="18" x2="6" y1="6" y2="18"/><line x1="6" x2="18" y1="6" y2="18"/></Icon>
        );
        const Save = (props) => (
            <Icon {...props}><path d="M19 21H5a2 2 0 0 1-2-2V5a2 2 0 0 1 2-2h11l5 5v11a2 2 0 0 1-2 2z"/><polyline points="17 21 17 13 7 13 7 21"/><polyline points="7 3 7 8 15 8"/></Icon>
        );
        const LogOut = (props) => (
            <Icon {...props}><path d="M9 21H5a2 2 0 0 1-2-2V5a2 2 0 0 1 2-2h4"/><polyline points="16 17 21 12 16 7"/><line x1="21" x2="9" y1="12" y2="12"/></Icon>
        );
        const Plus = (props) => (
            <Icon {...props}><line x1="12" x2="12" y1="5" y2="19"/><line x1="5" x2="19" y1="12" y2="12"/></Icon>
        );
        const Trash2 = (props) => (
            <Icon {...props}><path d="M3 6h18"/><path d="M19 6v14c0 1-1 2-2 2H7c-1 0-2-1-2-2V6"/><path d="M8 6V4c0-1 1-2 2-2h4c1 0 2 1 2 2v2"/><line x1="10" x2="10" y1="11" y2="17"/><line x1="14" x2="14" y1="11" y2="17"/></Icon>
        );
        const MoveVertical = (props) => (
            <Icon {...props}><polyline points="8 18 12 22 16 18"/><polyline points="8 6 12 2 16 6"/><line x1="12" x2="12" y1="2" y2="22"/></Icon>
        );
        const GripVertical = (props) => (
            <Icon {...props}><circle cx="9" cy="5" r="1"/><circle cx="9" cy="12" r="1"/><circle cx="9" cy="19" r="1"/><circle cx="15" cy="5" r="1"/><circle cx="15" cy="12" r="1"/><circle cx="15" cy="19" r="1"/></Icon>
        );
        const LinkIcon = (props) => (
            <Icon {...props}><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"/><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"/></Icon>
        );

        const IconMap = {
            Instagram: <Instagram size={24} />,
            Twitch: <Twitch size={24} />,
            Youtube: <Youtube size={24} />,
            Send: <Send size={24} />,
            Music2: <Music2 size={24} />,
            Gamepad2: <Gamepad2 size={24} />,
            Mail: <Mail size={24} />,
            ExternalLink: <ExternalLink size={24} />,
        };

        const SocialIconMap = {
            Instagram: <Instagram size={20} />,
            Twitch: <Twitch size={20} />,
            Youtube: <Youtube size={20} />,
            Send: <Send size={20} />,
            Music2: <Music2 size={20} />,
            Gamepad2: <Gamepad2 size={20} />,
            Mail: <Mail size={20} />,
        };

        const DEFAULT_CONFIG = {
            title: '',
            handle: '@LuizinhoSouzaK',
            bgImage: 'https://images.unsplash.com/photo-1550745165-9bc0b252726f?q=80&w=2070&auto=format&fit=crop',
            bgPosition: 50,
            profileImage: 'https://picsum.photos/seed/profile/200',
            profileName: 'Luizinho Souza K ™',
            profileBio: '(@LuizinhoSouzaK) • Fotos y vídeos de Instagram',
            youtubeVideoId: 'z0zxcFHCYOM',
            youtubeStartTime: 210,
            links: [
                { id: '1', label: 'Instagram', url: '#', icon: 'Instagram' },
                { id: '2', label: 'Twitch', url: '#', icon: 'Twitch' },
                { id: '3', label: 'Youtube', url: '#', icon: 'Youtube' },
            ],
            socialLinks: [
                { id: 's1', label: 'Youtube', url: '#', icon: 'Youtube' },
                { id: 's2', label: 'Steam', url: '#', icon: 'Gamepad2' },
                { id: 's3', label: 'Instagram', url: '#', icon: 'Instagram' },
                { id: 's4', label: 'Twitch', url: '#', icon: 'Twitch' },
                { id: 's5', label: 'Telegram', url: '#', icon: 'Send' },
                { id: 's6', label: 'Spotify', url: '#', icon: 'Music2' },
            ],
            secondaryButtonText: 'Desenvolvido por LZKtech',
            secondaryButtonUrl: '#',
            newsletterTitle: 'Subscribe to LuizinhoSouzaK',
            newsletterSubtitle: 'Sign up to get exclusive email updates directly from me.'
        };

        function App() {
            const [config, setConfig] = useState(DEFAULT_CONFIG);
            const [isAdminMode, setIsAdminMode] = useState(false);
            const [isLoginOpen, setIsLoginOpen] = useState(false);
            const [loginForm, setLoginForm] = useState({ user: '', pass: '' });
            const fileInputRef = useRef(null);
            const profileInputRef = useRef(null);

            useEffect(() => {
                const saved = localStorage.getItem('holl_the_fame_config');
                if (saved) {
                    try {
                        const parsed = JSON.parse(saved);
                        if (parsed.links) {
                            parsed.links = parsed.links.map((l, i) => ({
                                ...l,
                                id: l.id || `link-${Date.now()}-${i}`
                            }));
                        }
                        if (!parsed.socialLinks) {
                            parsed.socialLinks = DEFAULT_CONFIG.socialLinks;
                        }
                        if (!parsed.secondaryButtonText) {
                            parsed.secondaryButtonText = DEFAULT_CONFIG.secondaryButtonText;
                            parsed.secondaryButtonUrl = DEFAULT_CONFIG.secondaryButtonUrl;
                            parsed.newsletterTitle = DEFAULT_CONFIG.newsletterTitle;
                            parsed.newsletterSubtitle = DEFAULT_CONFIG.newsletterSubtitle;
                        }
                        // Migration: Clear old title if it exists
                        if (parsed.title === 'Holl The Fame LZK') {
                            parsed.title = '';
                        }
                        setConfig(parsed);
                    } catch (e) {
                        console.error("Failed to load config", e);
                    }
                }
            }, []);

            const saveConfig = (newConfig) => {
                setConfig(newConfig);
                localStorage.setItem('holl_the_fame_config', JSON.stringify(newConfig));
            };

            const handleLogin = (e) => {
                e.preventDefault();
                if (loginForm.user === 'luizinho' && loginForm.pass === 'Pastel30') {
                    setIsAdminMode(true);
                    setIsLoginOpen(false);
                    setLoginForm({ user: '', pass: '' });
                } else {
                    alert('Acesso negado!!');
                }
            };

            const handleBgUpload = (e) => {
                const file = e.target.files?.[0];
                if (file) {
                    const reader = new FileReader();
                    reader.onloadend = () => {
                        saveConfig({ ...config, bgImage: reader.result });
                    };
                    reader.readAsDataURL(file);
                }
            };

            const handleProfileUpload = (e) => {
                const file = e.target.files?.[0];
                if (file) {
                    const reader = new FileReader();
                    reader.onloadend = () => {
                        saveConfig({ ...config, profileImage: reader.result });
                    };
                    reader.readAsDataURL(file);
                }
            };

            const onDragEnd = (result) => {
                if (!result.destination) return;
                const items = Array.from(config.links);
                const [reorderedItem] = items.splice(result.source.index, 1);
                items.splice(result.destination.index, 0, reorderedItem);
                saveConfig({ ...config, links: items });
            };

            return (
                <div className="min-h-screen bg-[#0a0a0a] text-white font-sans selection:bg-red-500/30 overflow-x-hidden">
                    {/* Background Image Header */}
                    <div className="relative h-[40vh] sm:h-[45vh] w-full overflow-hidden">
                        <motion.div 
                            initial={{ scale: 1.1, opacity: 0 }}
                            animate={{ scale: 1, opacity: 1 }}
                            transition={{ duration: 1.2 }}
                            className="absolute inset-0"
                        >
                            <img 
                                src={config.bgImage} 
                                alt="Background" 
                                className="w-full h-full object-cover"
                                style={{ objectPosition: `center ${config.bgPosition}%` }}
                                referrerPolicy="no-referrer"
                            />
                            <div className="absolute inset-0 bg-gradient-to-b from-transparent via-transparent to-[#0a0a0a]" />
                        </motion.div>

                        {/* Top Controls */}
                        <div className="absolute top-4 left-4 right-4 z-20 flex justify-between items-center">
                            <button 
                                className="p-2 bg-black/40 backdrop-blur-md rounded-full border border-white/20 hover:bg-black/60 transition-all group"
                                title="Compartilhar"
                                onClick={() => {
                                    if (navigator.share) {
                                        navigator.share({
                                            title: config.title,
                                            url: window.location.href
                                        });
                                    }
                                }}
                            >
                                <Send size={20} className="text-white/80 group-hover:text-white -rotate-45" />
                            </button>

                            <div className="flex gap-2">
                                {isAdminMode ? (
                                    <button 
                                        onClick={() => setIsAdminMode(false)}
                                        className="flex items-center gap-2 px-4 py-2 bg-red-600 rounded-full border border-white/40 hover:bg-red-700 transition-all font-bold text-xs sm:text-sm shadow-lg"
                                    >
                                        <LogOut size={16} />
                                        Sair Admin
                                    </button>
                                ) : (
                                    <button 
                                        onClick={() => setIsLoginOpen(true)}
                                        className="p-2 bg-black/40 backdrop-blur-md rounded-full border border-white/20 hover:bg-black/60 transition-all group"
                                        title="Admin"
                                    >
                                        <Settings size={20} className="text-white/80 group-hover:text-white" />
                                    </button>
                                )}
                            </div>
                        </div>

                        <div className="absolute bottom-8 left-0 right-0 text-center z-10 px-4">
                            {config.title && (
                                <motion.h1 
                                    initial={{ y: 20, opacity: 0 }}
                                    animate={{ y: 0, opacity: 1 }}
                                    transition={{ delay: 0.5 }}
                                    className="text-3xl sm:text-4xl md:text-6xl font-display font-bold tracking-tighter uppercase break-words"
                                >
                                    {config.title}
                                </motion.h1>
                            )}
                            <motion.p
                                initial={{ y: 10, opacity: 0 }}
                                animate={{ y: 0, opacity: 1 }}
                                transition={{ delay: 0.6 }}
                                className="text-white/60 font-medium tracking-widest text-xs sm:text-sm mt-1"
                            >
                                {config.handle}
                            </motion.p>
                            
                            <motion.div 
                                initial={{ y: 20, opacity: 0 }}
                                animate={{ y: 0, opacity: 1 }}
                                transition={{ delay: 0.7 }}
                                className="flex justify-center flex-wrap gap-3 sm:gap-4 mt-6 px-4"
                            >
                                {config.socialLinks.map((social, index) => (
                                    <div key={social.id} className="relative group/social">
                                        <a 
                                            href={isAdminMode ? undefined : social.url} 
                                            className={`text-white/80 hover:text-white hover:scale-110 transition-all block p-1 ${isAdminMode ? 'cursor-default' : 'cursor-pointer'}`}
                                            title={social.label}
                                            target="_blank"
                                            rel="noopener noreferrer"
                                        >
                                            {SocialIconMap[social.icon] || <ExternalLink size={20} />}
                                        </a>
                                        
                                        {isAdminMode && (
                                            <div className="absolute -top-8 left-1/2 -translate-x-1/2 bg-black/80 backdrop-blur-md border border-white/20 rounded-lg p-2 flex gap-2 opacity-0 group-hover/social:opacity-100 transition-opacity z-30">
                                                <button 
                                                    onClick={() => {
                                                        const url = prompt('URL do Social:', social.url);
                                                        if (url !== null) {
                                                            const newSocials = [...config.socialLinks];
                                                            newSocials[index].url = url;
                                                            saveConfig({ ...config, socialLinks: newSocials });
                                                        }
                                                    }}
                                                    className="p-1 hover:bg-white/10 rounded"
                                                    title="Editar Link"
                                                >
                                                    <LinkIcon size={12} />
                                                </button>
                                                <button 
                                                    onClick={() => {
                                                        const icon = prompt('Ícone (Instagram, Twitch, Youtube, Send, Music2, Gamepad2, Mail):', social.icon);
                                                        if (icon && SocialIconMap[icon]) {
                                                            const newSocials = [...config.socialLinks];
                                                            newSocials[index].icon = icon;
                                                            saveConfig({ ...config, socialLinks: newSocials });
                                                        }
                                                    }}
                                                    className="p-1 hover:bg-white/10 rounded"
                                                    title="Mudar Ícone"
                                                >
                                                    <ImageIcon size={12} />
                                                </button>
                                                <button 
                                                    onClick={() => {
                                                        const newSocials = [...config.socialLinks];
                                                        newSocials.splice(index, 1);
                                                        saveConfig({ ...config, socialLinks: newSocials });
                                                    }}
                                                    className="p-1 hover:bg-red-500/20 text-red-400 rounded"
                                                    title="Excluir"
                                                >
                                                    <Trash2 size={12} />
                                                </button>
                                            </div>
                                        )}
                                    </div>
                                ))}
                                
                                {isAdminMode && (
                                    <button 
                                        onClick={() => {
                                            const label = prompt('Nome (ex: Instagram):');
                                            const url = prompt('URL:');
                                            const icon = prompt('Ícone (Instagram, Twitch, Youtube, Send, Music2, Gamepad2, Mail):', 'Instagram');
                                            if (label && url && icon) {
                                                const newSocial = {
                                                    id: `social-${Date.now()}`,
                                                    label,
                                                    url,
                                                    icon
                                                };
                                                saveConfig({ ...config, socialLinks: [...config.socialLinks, newSocial] });
                                            }
                                        }}
                                        className="text-white/40 hover:text-white transition-all p-1"
                                        title="Adicionar Social"
                                    >
                                        <Plus size={20} />
                                    </button>
                                )}
                            </motion.div>
                        </div>
                    </div>

                    {/* Content Section */}
                    <main className="max-w-md mx-auto px-4 sm:px-6 pb-32 sm:pb-20 -mt-4 relative z-20">
                        <div className="space-y-4">
                            <DragDropContext onDragEnd={onDragEnd}>
                                <Droppable droppableId="links">
                                    {(provided) => (
                                        <div {...provided.droppableProps} ref={provided.innerRef} className="space-y-4">
                                            {config.links.map((link, index) => (
                                                <Draggable key={link.id} draggableId={link.id} index={index} isDragDisabled={!isAdminMode}>
                                                    {(provided, snapshot) => (
                                                        <div
                                                            ref={provided.innerRef}
                                                            {...provided.draggableProps}
                                                            className={`relative group ${snapshot.isDragging ? 'z-50' : ''}`}
                                                        >
                                                            <motion.div
                                                                initial={{ x: -20, opacity: 0 }}
                                                                animate={{ x: 0, opacity: 1 }}
                                                                transition={{ delay: 0.1 * index }}
                                                                className={`flex flex-col p-4 rounded-3xl border-2 border-white bg-[#7a1010] shadow-xl transition-all ${!isAdminMode ? 'hover:scale-[1.02] active:scale-[0.98]' : ''}`}
                                                            >
                                                                <div className="flex items-center justify-between w-full">
                                                                    <div className="flex items-center gap-4 flex-1">
                                                                        {isAdminMode && (
                                                                            <div {...provided.dragHandleProps} className="cursor-grab active:cursor-grabbing p-1 text-white/40 hover:text-white">
                                                                                <GripVertical size={20} />
                                                                            </div>
                                                                        )}
                                                                        <a 
                                                                            href={isAdminMode ? undefined : link.url} 
                                                                            className={`flex items-center gap-4 flex-1 ${isAdminMode ? 'cursor-default' : 'cursor-pointer'}`}
                                                                            target="_blank"
                                                                            rel="noopener noreferrer"
                                                                        >
                                                                            <span className="p-2 bg-black/10 rounded-xl group-hover:bg-black/20 transition-colors shrink-0">
                                                                                {IconMap[link.icon] || <ExternalLink size={24} />}
                                                                            </span>
                                                                            {isAdminMode ? (
                                                                                <input 
                                                                                    className="bg-black/20 border border-white/20 rounded px-2 py-1 w-full text-lg font-semibold focus:border-white/40 outline-none"
                                                                                    value={link.label}
                                                                                    onChange={(e) => {
                                                                                        const newLinks = [...config.links];
                                                                                        newLinks[index].label = e.target.value;
                                                                                        saveConfig({ ...config, links: newLinks });
                                                                                    }}
                                                                                />
                                                                            ) : (
                                                                                <span className="font-semibold text-lg truncate">{link.label}</span>
                                                                            )}
                                                                        </a>
                                                                    </div>
                                                                    {!isAdminMode && <ExternalLink size={18} className="opacity-40 group-hover:opacity-100 transition-opacity shrink-0 ml-2" />}
                                                                    
                                                                    {isAdminMode && (
                                                                        <button 
                                                                            onClick={() => {
                                                                                const newLinks = [...config.links];
                                                                                newLinks.splice(index, 1);
                                                                                saveConfig({ ...config, links: newLinks });
                                                                            }}
                                                                            className="p-2 bg-red-600/20 hover:bg-red-600 rounded-full transition-all text-white/60 hover:text-white shrink-0 ml-2"
                                                                        >
                                                                            <Trash2 size={18} />
                                                                        </button>
                                                                    )}
                                                                </div>

                                                                {isAdminMode && (
                                                                    <div className="mt-3 flex items-center gap-2 pl-10">
                                                                        <LinkIcon size={14} className="text-white/40 shrink-0" />
                                                                        <input 
                                                                            className="bg-black/20 border border-white/20 rounded px-2 py-1 w-full text-xs text-white/60 focus:border-white/40 outline-none"
                                                                            value={link.url}
                                                                            placeholder="URL do Link"
                                                                            onChange={(e) => {
                                                                                const newLinks = [...config.links];
                                                                                newLinks[index].url = e.target.value;
                                                                                saveConfig({ ...config, links: newLinks });
                                                                            }}
                                                                        />
                                                                    </div>
                                                                )}
                                                            </motion.div>
                                                        </div>
                                                    )}
                                                </Draggable>
                                            ))}
                                            {provided.placeholder}
                                        </div>
                                    )}
                                </Droppable>
                            </DragDropContext>

                            {isAdminMode && (
                                <button 
                                    onClick={() => {
                                        const label = prompt('Nome do Link:');
                                        const url = prompt('URL do Link:');
                                        if (label && url) {
                                            const newLink = {
                                                id: `link-${Date.now()}`,
                                                label,
                                                url,
                                                icon: 'ExternalLink'
                                            };
                                            saveConfig({ ...config, links: [...config.links, newLink] });
                                        }
                                    }}
                                    className="w-full flex items-center justify-center gap-2 p-5 rounded-3xl border-2 border-dashed border-white/40 hover:border-white/60 hover:bg-white/5 transition-all text-white/60 font-bold"
                                >
                                    <Plus size={24} /> Adicionar Novo Botão
                                </button>
                            )}

                            {/* Profile Card */}
                            <motion.div
                                initial={{ y: 20, opacity: 0 }}
                                animate={{ y: 0, opacity: 1 }}
                                transition={{ delay: 1.2 }}
                                className="bg-[#7a1010] p-6 rounded-3xl border-2 border-white flex items-center gap-4 relative shadow-xl"
                            >
                                <div 
                                    className={`w-16 h-16 rounded-full overflow-hidden border-2 border-white/20 flex-shrink-0 ${isAdminMode ? 'cursor-pointer hover:opacity-80 ring-2 ring-white/40' : ''}`}
                                    onClick={() => isAdminMode && profileInputRef.current?.click()}
                                >
                                    <img 
                                        src={config.profileImage} 
                                        alt="Profile" 
                                        className="w-full h-full object-cover"
                                        referrerPolicy="no-referrer"
                                    />
                                </div>
                                <div className="flex-1 min-w-0">
                                    {isAdminMode ? (
                                        <div className="space-y-1">
                                            <input 
                                                className="bg-black/20 border border-white/20 rounded px-2 py-1 w-full text-sm font-bold outline-none focus:border-white/40"
                                                value={config.profileName}
                                                onChange={(e) => saveConfig({ ...config, profileName: e.target.value })}
                                            />
                                            <textarea 
                                                className="bg-black/20 border border-white/20 rounded px-2 py-1 w-full text-xs text-white/70 outline-none focus:border-white/40 resize-none"
                                                rows={2}
                                                value={config.profileBio}
                                                onChange={(e) => saveConfig({ ...config, profileBio: e.target.value })}
                                            />
                                        </div>
                                    ) : (
                                        <>
                                            <h3 className="font-bold text-lg leading-tight truncate">{config.profileName}</h3>
                                            <p className="text-white/70 text-sm line-clamp-2">{config.profileBio}</p>
                                        </>
                                    )}
                                </div>
                                <input type="file" ref={profileInputRef} className="hidden" onChange={handleProfileUpload} accept="image/*" />
                            </motion.div>

                            {/* Secondary Button */}
                            <motion.div
                                initial={{ y: 20, opacity: 0 }}
                                animate={{ y: 0, opacity: 1 }}
                                transition={{ delay: 1.3 }}
                                className="relative group/secondary"
                            >
                                <a
                                    href={isAdminMode ? undefined : config.secondaryButtonUrl}
                                    target="_blank"
                                    rel="noopener noreferrer"
                                    className="w-full flex items-center justify-center gap-3 p-4 rounded-3xl border-2 border-white bg-[#7a1010] hover:bg-[#8a1a1a] transition-all shadow-xl"
                                >
                                    <Users size={24} />
                                    {isAdminMode ? (
                                        <input 
                                            className="bg-black/20 border border-white/20 rounded px-2 py-1 flex-1 text-center font-semibold outline-none focus:border-white/40"
                                            value={config.secondaryButtonText}
                                            onChange={(e) => saveConfig({ ...config, secondaryButtonText: e.target.value })}
                                        />
                                    ) : (
                                        <span className="font-semibold">{config.secondaryButtonText}</span>
                                    )}
                                </a>
                                
                                {isAdminMode && (
                                    <div className="absolute -top-10 left-1/2 -translate-x-1/2 bg-black/80 backdrop-blur-md border border-white/20 rounded-lg p-2 flex gap-2 opacity-0 group-hover/secondary:opacity-100 transition-opacity z-30">
                                        <div className="flex items-center gap-2 px-2">
                                            <LinkIcon size={14} className="text-white/40" />
                                            <input 
                                                className="bg-black/20 border border-white/20 rounded px-2 py-1 text-xs w-48 outline-none focus:border-white/40"
                                                value={config.secondaryButtonUrl}
                                                placeholder="URL do Botão"
                                                onChange={(e) => saveConfig({ ...config, secondaryButtonUrl: e.target.value })}
                                            />
                                        </div>
                                    </div>
                                )}
                            </motion.div>

                            {/* Newsletter Section */}
                            <motion.div
                                initial={{ y: 20, opacity: 0 }}
                                animate={{ y: 0, opacity: 1 }}
                                transition={{ delay: 1.4 }}
                                className="bg-[#7a1010] p-6 sm:p-8 rounded-[2.5rem] border-2 border-white text-center space-y-6 shadow-xl"
                            >
                                <div className="space-y-2">
                                    {isAdminMode ? (
                                        <div className="space-y-2">
                                            <input 
                                                className="bg-black/20 border border-white/20 rounded px-2 py-1 w-full text-xl sm:text-2xl font-bold text-center outline-none focus:border-white/40"
                                                value={config.newsletterTitle}
                                                onChange={(e) => saveConfig({ ...config, newsletterTitle: e.target.value })}
                                            />
                                            <textarea 
                                                className="bg-black/20 border border-white/20 rounded px-2 py-1 w-full text-xs sm:text-sm text-white/70 text-center outline-none focus:border-white/40 resize-none"
                                                rows={2}
                                                value={config.newsletterSubtitle}
                                                onChange={(e) => saveConfig({ ...config, newsletterSubtitle: e.target.value })}
                                            />
                                        </div>
                                    ) : (
                                        <>
                                            <h2 className="text-xl sm:text-2xl font-bold tracking-tight">{config.newsletterTitle}</h2>
                                            <p className="text-white/70 text-xs sm:text-sm">{config.newsletterSubtitle}</p>
                                        </>
                                    )}
                                </div>
                                
                                <div className="space-y-3">
                                    <input 
                                        type="text" 
                                        placeholder="First Name" 
                                        className="w-full bg-transparent border-2 border-white rounded-2xl p-4 focus:border-white/40 outline-none transition-all placeholder:text-white/30 text-sm"
                                    />
                                    <input 
                                        type="email" 
                                        placeholder="Email" 
                                        className="w-full bg-transparent border-2 border-white rounded-2xl p-4 focus:border-white/40 outline-none transition-all placeholder:text-white/30 text-sm"
                                    />
                                    <button className="w-full bg-white text-[#7a1010] font-bold py-4 rounded-2xl hover:bg-white/90 active:scale-[0.98] transition-all shadow-lg">
                                        Subscribe
                                    </button>
                                </div>
                            </motion.div>

                            {/* YouTube Featured Video Card */}
                            <motion.div
                                initial={{ y: 20, opacity: 0 }}
                                animate={{ y: 0, opacity: 1 }}
                                transition={{ delay: 1.5 }}
                                className="bg-white rounded-3xl overflow-hidden shadow-2xl border-2 border-white relative"
                            >
                                <div className="aspect-video w-full bg-black">
                                    <iframe
                                        className="w-full h-full"
                                        src={`https://www.youtube.com/embed/${config.youtubeVideoId}?start=${config.youtubeStartTime}`}
                                        title="YouTube video player"
                                        frameBorder="0"
                                        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
                                        allowFullScreen
                                    ></iframe>
                                </div>
                                <div className="p-5 sm:p-6 space-y-4">
                                    <div className="flex items-center gap-3">
                                        <div className="w-10 h-10 rounded-full bg-red-100 flex items-center justify-center text-red-600 shrink-0">
                                            <Youtube size={20} />
                                        </div>
                                        <div className="min-w-0">
                                            <h4 className="text-black font-bold text-lg truncate">LZK Tech <span className="text-gray-400 font-normal ml-1">no YouTube</span></h4>
                                        </div>
                                    </div>
                                    
                                    {isAdminMode ? (
                                        <div className="space-y-2">
                                            <div className="flex flex-col sm:flex-row gap-2">
                                                <div className="flex-1 space-y-1">
                                                    <label className="text-[10px] text-black/40 font-bold uppercase">ID do Vídeo</label>
                                                    <input 
                                                        placeholder="Video ID"
                                                        className="w-full bg-gray-100 border border-gray-300 rounded px-3 py-2 text-black text-sm outline-none focus:border-red-500"
                                                        value={config.youtubeVideoId}
                                                        onChange={(e) => saveConfig({ ...config, youtubeVideoId: e.target.value })}
                                                    />
                                                </div>
                                                <div className="w-full sm:w-24 space-y-1">
                                                    <label className="text-[10px] text-black/40 font-bold uppercase">Início (s)</label>
                                                    <input 
                                                        placeholder="Start (s)"
                                                        type="number"
                                                        className="w-full bg-gray-100 border border-gray-300 rounded px-3 py-2 text-black text-sm outline-none focus:border-red-500"
                                                        value={config.youtubeStartTime}
                                                        onChange={(e) => saveConfig({ ...config, youtubeStartTime: parseInt(e.target.value) || 0 })}
                                                    />
                                                </div>
                                            </div>
                                        </div>
                                    ) : (
                                        <p className="text-gray-800 font-medium text-base sm:text-lg leading-snug">
                                            Assista aos vídeos mais recentes e novidades de tecnologia!
                                        </p>
                                    )}

                                    <a 
                                        href="https://www.youtube.com/@LZKTech" 
                                        target="_blank" 
                                        rel="noopener noreferrer"
                                        className="flex items-center justify-between pt-4 border-t border-gray-100 group"
                                    >
                                        <div className="flex items-center gap-2 text-red-600 font-bold text-sm group-hover:underline truncate">
                                            <div className="w-2 h-2 rounded-full bg-red-600 animate-pulse shrink-0" />
                                            Acessar @LZKTech
                                        </div>
                                        <div className="flex items-center gap-1 text-gray-400 text-[10px] font-bold uppercase tracking-wider shrink-0">
                                            <ExternalLink size={14} />
                                            YouTube
                                        </div>
                                    </a>
                                </div>
                            </motion.div>
                        </div>

                        {/* Footer */}
                        <footer className="mt-16 text-center space-y-6">
                            <div className="flex flex-col items-center gap-2 opacity-60">
                                <div className="flex items-center gap-2">
                                    <div className="w-8 h-8 rounded-full bg-red-600 flex items-center justify-center shadow-lg shadow-red-600/20">
                                        <Youtube size={16} className="text-white" />
                                    </div>
                                    <span className="font-bold text-xl tracking-tighter">LZK</span>
                                </div>
                            </div>
                            
                            <div className="inline-flex items-center gap-4 bg-white/5 backdrop-blur-sm border border-white/10 rounded-full px-6 py-3 text-xs sm:text-sm font-medium">
                                <span className="flex items-center gap-2">
                                    <div className="w-5 h-5 rounded-full bg-red-600/20 flex items-center justify-center">
                                        <Youtube size={10} className="text-red-500" />
                                    </div>
                                    LZK
                                </span>
                                <span className="w-px h-4 bg-white/20" />
                                <span className="text-white/60">Try for free!</span>
                            </div>
                        </footer>
                    </main>

                    {/* Admin Overlay Controls */}
                    <AnimatePresence>
                        {isAdminMode && (
                            <motion.div 
                                initial={{ y: 100 }}
                                animate={{ y: 0 }}
                                exit={{ y: 100 }}
                                className="fixed bottom-0 left-0 right-0 bg-black/90 backdrop-blur-2xl border-t border-white/20 p-4 sm:p-6 z-[60] flex flex-col sm:flex-row justify-center gap-4 sm:gap-6 items-center shadow-2xl"
                            >
                                <div className="flex items-center gap-3 sm:gap-4 w-full sm:w-auto justify-between">
                                    <button 
                                        onClick={() => fileInputRef.current?.click()}
                                        className="flex items-center gap-2 px-4 py-2 bg-white text-black rounded-full font-bold hover:bg-white/90 transition-all text-xs sm:text-sm shadow-lg"
                                    >
                                        <ImageIcon size={18} /> Fundo
                                    </button>
                                    <div className="flex items-center gap-2 bg-white/10 rounded-full px-4 py-2 flex-1 sm:flex-none">
                                        <MoveVertical size={18} className="text-white/60 shrink-0" />
                                        <input 
                                            type="range" 
                                            min="0" max="100" 
                                            value={config.bgPosition} 
                                            onChange={(e) => saveConfig({ ...config, bgPosition: parseInt(e.target.value) })}
                                            className="w-full sm:w-24 accent-white cursor-pointer"
                                        />
                                        <span className="text-[10px] font-mono w-8 text-right shrink-0">{config.bgPosition}%</span>
                                    </div>
                                </div>

                                <div className="flex items-center gap-3 sm:gap-4 border-t sm:border-t-0 sm:border-l border-white/20 pt-4 sm:pt-0 sm:pl-6 w-full sm:w-auto">
                                    <div className="flex-1 sm:flex-none space-y-1">
                                        <label className="text-[9px] uppercase tracking-widest text-white/40 font-bold">Título</label>
                                        <input 
                                            className="bg-white/10 border border-white/20 rounded px-3 py-1 text-xs w-full sm:w-40 outline-none focus:border-white/40"
                                            value={config.title}
                                            onChange={(e) => saveConfig({ ...config, title: e.target.value })}
                                        />
                                    </div>
                                    <div className="flex-1 sm:flex-none space-y-1">
                                        <label className="text-[9px] uppercase tracking-widest text-white/40 font-bold">Handle</label>
                                        <input 
                                            className="bg-white/10 border border-white/20 rounded px-3 py-1 text-xs w-full sm:w-32 outline-none focus:border-white/40"
                                            value={config.handle}
                                            onChange={(e) => saveConfig({ ...config, handle: e.target.value })}
                                        />
                                    </div>
                                </div>

                                <button 
                                    onClick={() => {
                                        saveConfig(config);
                                        alert('Alterações salvas com sucesso!');
                                    }}
                                    className="flex items-center gap-2 px-6 py-2 bg-green-600 rounded-full font-bold hover:bg-green-700 transition-all w-full sm:w-auto justify-center text-xs sm:text-sm shadow-lg"
                                >
                                    <Save size={18} /> Salvar Tudo
                                </button>
                                <input type="file" ref={fileInputRef} className="hidden" onChange={handleBgUpload} accept="image/*" />
                            </motion.div>
                        )}
                    </AnimatePresence>

                    {/* Login Modal */}
                    <AnimatePresence>
                        {isLoginOpen && (
                            <motion.div 
                                initial={{ opacity: 0 }}
                                animate={{ opacity: 1 }}
                                exit={{ opacity: 0 }}
                                className="fixed inset-0 z-[100] flex items-center justify-center p-4 sm:p-6 bg-black/80 backdrop-blur-md"
                            >
                                <motion.div 
                                    initial={{ scale: 0.9, y: 20 }}
                                    animate={{ scale: 1, y: 0 }}
                                    className="bg-[#1a1a1a] border-2 border-white/20 rounded-[2rem] p-6 sm:p-8 w-full max-w-sm shadow-2xl relative overflow-hidden"
                                >
                                    <div className="absolute top-0 left-0 w-full h-1 bg-gradient-to-r from-red-600 via-white to-red-600" />
                                    
                                    <button 
                                        onClick={() => setIsLoginOpen(false)}
                                        className="absolute top-4 right-4 text-white/40 hover:text-white transition-colors"
                                    >
                                        <X size={24} />
                                    </button>

                                    <div className="text-center mb-8">
                                        <div className="w-16 h-16 bg-red-600 rounded-2xl mx-auto flex items-center justify-center shadow-lg shadow-red-600/20 mb-4 rotate-3">
                                            <Settings size={32} className="text-white" />
                                        </div>
                                        <h2 className="text-2xl font-display font-bold">Admin Login</h2>
                                        <p className="text-white/40 text-sm mt-1">Acesso restrito ao painel</p>
                                    </div>

                                    <form onSubmit={handleLogin} className="space-y-4">
                                        <div className="space-y-1">
                                            <label className="text-[10px] uppercase tracking-widest text-white/40 font-bold ml-1">Usuário</label>
                                            <input 
                                                type="text"
                                                className="w-full bg-white/5 border-2 border-white/10 rounded-2xl p-4 focus:border-red-600 outline-none transition-all"
                                                value={loginForm.user}
                                                onChange={(e) => setLoginForm({ ...loginForm, user: e.target.value })}
                                            />
                                        </div>
                                        <div className="space-y-1">
                                            <label className="text-[10px] uppercase tracking-widest text-white/40 font-bold ml-1">Senha</label>
                                            <input 
                                                type="password"
                                                className="w-full bg-white/5 border-2 border-white/10 rounded-2xl p-4 focus:border-red-600 outline-none transition-all"
                                                value={loginForm.pass}
                                                onChange={(e) => setLoginForm({ ...loginForm, pass: e.target.value })}
                                            />
                                        </div>
                                        <button 
                                            type="submit"
                                            className="w-full bg-white text-black font-bold py-4 rounded-2xl hover:bg-red-600 hover:text-white transition-all shadow-lg active:scale-[0.98] mt-4"
                                        >
                                            Entrar no Painel
                                        </button>
                                    </form>
                                </motion.div>
                            </motion.div>
                        )}
                    </AnimatePresence>
                </div>
            );
        }

        const root = ReactDOM.createRoot(document.getElementById('root'));
        root.render(<App />);
    </script>
</body>
</html>
