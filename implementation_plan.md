# K-Sleep Onboarding Flow Implementation Plan

This project aims to build a premium, Calm-inspired sleep care onboarding flow tailored for the Korean market.

## Proposed Changes

### Configuration & Setup
- **Framework**: Next.js 14 (App Router)
- **Styling**: Tailwind CSS for rapid UI development with custom brand colors.
- **State**: Zustand for managing survey answers across steps.
- **Animations**: Framer Motion for smooth transitions (0.4s-0.5s).

### Brand Colors
Modified `tailwind.config.ts` or `globals.css` to include:
- Primary: `#A8C8E8` (Light Blue)
- Highlight: `#FCE7A2` (Warm Yellow)
- Neutral: `#BBA89A` (Taupe)
- Base: `#F5F6FA` (Off-white)
- Accent: `#FAD7C8` (Peach)
- Text/Dark: `#5C647C` (Deep Blue/Grey)

### Components

#### [NEW] `components/Onboarding/Background.tsx`
Full-screen background using the provided hero image with a dark overlay for readability.

#### [NEW] `components/Onboarding/QuestionStep.tsx`
A reusable component for each survey question with smooth entry/exit animations.

#### [NEW] `components/Onboarding/ProgressBar.tsx`
Visual indicator of progress at the top of the flow.

#### [NEW] `components/Onboarding/SocialLogins.tsx`
Premium styled buttons for Kakao, Naver, and Apple.

### Flow Logic
1. **Entry**: Splash screen with "편안한 잠의 요정" message.
2. **Questions**: 5-7 targeted questions about sleep habits.
3. **Processing**: Subtle animation indicating "Analyzing your sleep profile...".
4. **Persona**: Reveal the user's sleep persona (e.g., 예민한 올빼미형).
5. **Conversion**: Social login/Signup to see full results.

## Verification Plan

### Automated Tests
- N/A for MVP, focusing on visual verification.

### Manual Verification
- Check transition speeds (aim for 0.4s-0.5s).
- Verify dark theme aesthetics on all screens.
- Ensure the background image covers the screen without distortion.
- Test responsive layout on mobile-sized viewports (as sleep apps are primarily mobile).
