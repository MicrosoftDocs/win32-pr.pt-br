---
description: a partir do Windows 8, a \_ infraestrutura AppInit DLLs é desabilitada quando a inicialização segura está habilitada.
ms.assetid: 3ADE71C7-7113-4D26-8D6D-5609CAF13397
title: AppInit DLLs e inicialização segura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67db758eebbccd1916b5c2611c20598c3f4d25cc80cd2910be22a65b4222bbae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119256016"
---
# <a name="appinit-dlls-and-secure-boot"></a>AppInit DLLs e inicialização segura

a partir do Windows 8, a \_ infraestrutura AppInit DLLs é desabilitada quando a inicialização segura está habilitada.

## <a name="about-appinit_dlls"></a>Sobre \_ DLLs AppInit

A \_ infraestrutura AppInit DLLs fornece uma maneira fácil de conectar APIs do sistema, permitindo que DLLs personalizadas sejam carregadas no espaço de endereço de cada aplicativo interativo. Os aplicativos e os softwares mal-intencionados usam DLLs AppInit para o mesmo motivo básico, que é vincular APIs; Depois que a DLL personalizada é carregada, ela pode conectar uma API do sistema conhecida e implementar a funcionalidade alternativa. Apenas um pequeno conjunto de aplicativos legítimos modernos usa esse mecanismo para carregar DLLs, enquanto um grande conjunto de malwares usa esse mecanismo para comprometer sistemas. Até mesmo as DLLs AppInit legítimas \_ podem causar problemas de desempenho e deadlocks do sistema, portanto, o uso de \_ DLLs AppInit não é recomendado.

## <a name="appinit_dlls-and-secure-boot"></a>AppInit \_ DLLs e inicialização segura

Windows 8 adotou a UEFI e a inicialização segura para melhorar a integridade geral do sistema e para fornecer proteção forte contra ameaças sofisticadas. Quando a inicialização segura está habilitada, o \_ mecanismo de DLLs AppInit é desabilitado como parte de uma abordagem sem comprometimento para proteger os clientes contra malware e ameaças.

observe que a inicialização segura é um protocolo UEFI e não um recurso Windows 8. Mais informações sobre a UEFI e a especificação de protocolo de inicialização segura podem ser encontradas em [https://www.uefi.org](https://www.uefi.org/) .

## <a name="appinit_dlls-certification-requirement-for-windows-8-desktop-apps"></a>\_requisito de certificação AppInit DLLs para aplicativos de área de trabalho Windows 8

um dos requisitos de certificação para os aplicativos de área de trabalho Windows 8 é que o aplicativo não deve carregar DLLs arbitrárias para interceptar chamadas à API do Win32 usando o \_ mecanismo AppInit DLLs. para obter informações mais detalhadas sobre os requisitos de certificação, consulte a seção 1,1 de [requisitos de certificação para Windows 8 aplicativos de área de trabalho](../win_cert/certification-requirements-for-windows-desktop-apps.md).

## <a name="summary"></a>Resumo

-   O \_ mecanismo de DLLs AppInit não é uma abordagem recomendada para aplicativos legítimos porque pode levar a problemas de desempenho e deadlocks do sistema.
-   O \_ mecanismo AppInit DLLs é desabilitado por padrão quando a inicialização segura está habilitada.
-   o uso de \_ DLLs AppInit em um aplicativo de área de trabalho Windows 8 é uma falha de certificação de aplicativo de área de trabalho Windows.

consulte o white paper a seguir para obter informações sobre AppInit \_ dlls em Windows 7 e Windows server 2008 r2: [AppInit dlls no Windows 7 e Windows server 2008 r2](/previous-versions/windows/hardware/download/dn550976(v=vs.85)).

 

 
