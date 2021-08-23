---
title: Sobre as extensões do NPS
description: Esta seção descreve como implementar DLLs para estender a funcionalidade do NPS. Ele descreve a interação entre o NPS e as DLLs e apresenta algumas considerações de design sobre as DLLs.
ms.assetid: 3d4d8d22-4cd3-48e0-b4a4-dfa0a0b7b87f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 204fff8d97548e79eed3e317b3e14291e7288b55c51384c25ef8b912ad2d6095
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799456"
---
# <a name="about-nps-extensions"></a>Sobre as extensões do NPS

> [!Note]  
> o IAS (serviço de autenticação da Internet) foi renomeado como NPS (servidor de políticas de rede) a partir do Windows Server 2008. O conteúdo deste tópico aplica-se ao IAS e ao NPS. Em todo o texto, o NPS é usado para fazer referência a todas as versões do serviço, incluindo as versões originalmente chamadas de IAS.

 

Esta seção descreve como implementar DLLs para estender a funcionalidade do NPS. Ele descreve a interação entre o NPS e as DLLs e apresenta algumas considerações de design sobre as DLLs.

O NPS fornece dois pontos de extensão, um para autenticação e o outro para autorização. Autenticação refere-se à verificação da identidade do usuário. A autorização refere-se à determinação de quais serviços a rede deve fornecer ao usuário. Os dois pontos de extensão correspondem a DLLs de extensão de autenticação e DLLs de extensão de autorização. Cada ponto de extensão pode dar suporte a várias DLLs.

O NPS fornece serviços de autenticação e autorização. As DLLs de extensão de autenticação são chamadas pelo NPS antes da autenticação e autorização internas do NPS. As DLLs de extensão de autorização são chamadas após a autenticação e autorização do NPS.

O diagrama a seguir ilustra o fluxo de pacotes por meio de um servidor RADIUS NPS que é expandido usando DLLs de extensão.

![processo de autenticação e autorização do NPS](images/ias03.png)

Se um DLL de extensão de autenticação retornar ACCEPT, o pacote ignorará a autenticação NPS e vai diretamente para a autorização do NPS.

> [!Note]  
> Quando várias DLLs de extensão de autenticação estão presentes, o restante das DLLs de extensão também pode ser ignorado. Consulte [configurando as DLLs de extensão](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls) para obter mais informações.

 

Se uma DLL de extensão de autenticação retornar continuar, o pacote vai para a autenticação do NPS e, em seguida, para a autorização do NPS.

> [!Note]  
> Quando várias DLLs de extensão de autenticação estão presentes, o restante das DLLs de extensão de autenticação são invocadas antes da autenticação NPS.

 

Os tópicos a seguir descrevem as DLLs de extensão com mais detalhes:

-   [Configurando as DLLs de extensão](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls)
-   [Invocando as DLLs de extensão](/windows/desktop/Nps/ias-authentication-and-authorization-process)
-   [Atributos de identificação de usuário](/windows/desktop/Nps/ias-user-identification-attributes)

 

 