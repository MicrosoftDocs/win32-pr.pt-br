---
description: A partir Windows 8, a infraestrutura DLLs appInit \_ é desabilitada quando a inicialização segura está habilitada.
ms.assetid: 3ADE71C7-7113-4D26-8D6D-5609CAF13397
title: DLLs do AppInit e Inicialização Segura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67db758eebbccd1916b5c2611c20598c3f4d25cc80cd2910be22a65b4222bbae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119256016"
---
# <a name="appinit-dlls-and-secure-boot"></a>DLLs do AppInit e Inicialização Segura

A partir Windows 8, a infraestrutura DLLs appInit \_ é desabilitada quando a inicialização segura está habilitada.

## <a name="about-appinit_dlls"></a>Sobre DLLs do AppInit \_

A infraestrutura DLLs do AppInit fornece uma maneira fácil de conectar APIs do sistema permitindo que DLLs personalizadas sejam carregadas no espaço de endereço de \_ cada aplicativo interativo. Aplicativos e software mal-intencionado usam DLLs appInit pelo mesmo motivo básico, que é conectar APIs; depois que a DLL personalizada é carregada, ela pode conectar uma API de sistema conhecida e implementar funcionalidades alternativas. Somente um pequeno conjunto de aplicativos legítimos modernos usa esse mecanismo para carregar DLLs, enquanto um grande conjunto de malware usa esse mecanismo para comprometer sistemas. Até mesmo DLLs legítimas do AppInit podem causar involuções de deadlocks do sistema e problemas de desempenho, portanto, o uso de \_ DLLs do AppInit não \_ é recomendado.

## <a name="appinit_dlls-and-secure-boot"></a>DLLs do AppInit \_ e inicialização segura

Windows 8 UEFI e inicialização segura para melhorar a integridade geral do sistema e fornecer proteção forte contra ameaças sofisticadas. Quando a inicialização segura está habilitada, o mecanismo DLLs do AppInit é desabilitado como parte de uma abordagem sem comprometimento para proteger os clientes contra \_ malware e ameaças.

Observe que a inicialização segura é um protocolo UEFI e não um Windows 8 de segurança. Mais informações sobre UEFI e a especificação de protocolo de inicialização segura podem ser encontradas em [https://www.uefi.org](https://www.uefi.org/) .

## <a name="appinit_dlls-certification-requirement-for-windows-8-desktop-apps"></a>Requisito de certificação de DLLs do AppInit \_ para Windows 8 da área de trabalho

Um dos requisitos de certificação para Windows 8 da área de trabalho é que o aplicativo não deve carregar DLLs arbitrárias para interceptar chamadas à API win32 usando o mecanismo \_ DLLs do AppInit. Para obter informações mais detalhadas sobre os requisitos de certificação, consulte a seção 1.1 de Requisitos de certificação para Windows 8 da [área de trabalho.](../win_cert/certification-requirements-for-windows-desktop-apps.md)

## <a name="summary"></a>Resumo

-   O mecanismo DLLs do AppInit não é uma abordagem recomendada para aplicativos legítimos porque pode levar a deadlocks do sistema e problemas \_ de desempenho.
-   O mecanismo DLLs do AppInit é \_ desabilitado por padrão quando a inicialização segura está habilitada.
-   O uso de DLLs do AppInit em um aplicativo Windows 8 desktop é uma falha Windows de certificação do aplicativo da área \_ de trabalho.

Consulte o whitepaper a seguir para obter informações sobre DLLs do AppInit no Windows 7 e \_ Windows Server 2008 R2: [DLLs do AppInit no Windows 7 e Windows Server 2008 R2](/previous-versions/windows/hardware/download/dn550976(v=vs.85)).

 

 
