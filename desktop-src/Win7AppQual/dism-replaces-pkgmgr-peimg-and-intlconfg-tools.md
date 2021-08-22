---
description: DISM (Gerenciamento e Manutenção de Imagens de Implantação)
ms.assetid: bbfee966-121b-4b53-9e3e-08a747559da0
title: DISM (Gerenciamento e Manutenção de Imagens de Implantação)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b6da1cc8ec3e77a6c63df8e44917cb5f3474ae8e7a5e34b58f49255fa34b5b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053174"
---
# <a name="deployment-image-servicing-and-management-dism"></a>DISM (Gerenciamento e Manutenção de Imagens de Implantação)

## <a name="affected-platforms"></a>Plataformas afetadas

**Clientes** – Windows Vista SP1 e posterior \| Windows 7  
**Servidores** – Windows Server 2008 RTM e posterior \| Windows Server 2008 R2  


## <a name="description"></a>Descrição

A Gerenciamento e Manutenção de Imagens de Implantação (DISM) substitui as ferramentas pkgmgr, PEImg e IntlConfg que estão sendo Windows 7. O DISM fornece uma única ferramenta centralizada para executar todas as funções dessas três ferramentas de maneira mais eficiente e padronizada, eliminando a origem de muitas das frustrações experimentadas pelos usuários atuais dessas ferramentas.

O DISM inclui um shim para o Windows Vista SP1 e posterior, bem como para o Windows Server 2008 RTM e posterior, que redireciona chamadas pkgmgr de aplicativos herdado em execução no Windows 7 para o DISM. Se o aplicativo estiver em execução em um dos sistemas operacionais com suporte, o shim encaminha a chamada para pkgmgr. Não há shims para aplicativos herdado que chamam PEImg ou IntlConfg.

## <a name="usage"></a>Uso

O DISM é transparente para os usuários finais do pkgmgr em qualquer uma das plataformas com suporte. No entanto, se um aplicativo chamar PEImg ou IntlConfg Windows 7, a chamada falhará.

Atualize os scripts que chamam pkgmgr, PEImg ou IntlConfg para chamar o DISM. É importante incluir a atualização de scripts pkgmgr nesse esforço, pois o shim que fornece compatibilidade com versões anteriores para pkgmgr será removido em versões futuras dos sistemas operacionais Windows.

Verifique se as chamadas ao DISM substituiram todas as chamadas para pkgmgr, PEImg e IntlConfg e se a operação foi executada com êxito.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciamento e Manutenção de Imagens de Implantação (TechNet)](/previous-versions/windows/it-pro/windows-7/dd744256(v=ws.10))
</dt> </dl>

 

 
