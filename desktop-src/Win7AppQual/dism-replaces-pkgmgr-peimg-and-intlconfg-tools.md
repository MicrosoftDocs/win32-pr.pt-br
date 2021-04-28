---
description: DISM (Gerenciamento e Manutenção de Imagens de Implantação)
ms.assetid: bbfee966-121b-4b53-9e3e-08a747559da0
title: DISM (Gerenciamento e Manutenção de Imagens de Implantação)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 234d16233927dca2d5dba296fd33fb64135f691e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088484"
---
# <a name="deployment-image-servicing-and-management-dism"></a>DISM (Gerenciamento e Manutenção de Imagens de Implantação)

## <a name="affected-platforms"></a>Plataformas afetadas

**Clientes** -Windows Vista SP1 e \| Windows 7 posterior  
**Servidores** -windows Server 2008 RTM e posterior \| Windows Server 2008 R2  


## <a name="description"></a>Descrição

A ferramenta DISM (gerenciamento e manutenção de imagens de implantação) substitui as ferramentas pkgmgr, PEImg e IntlConfg que estão sendo desativadas no Windows 7. O DISM fornece uma única ferramenta centralizada para executar todas as funções dessas três ferramentas de maneira mais eficiente e padronizada, eliminando a origem de muitas das frustrações experimentadas pelos usuários atuais dessas ferramentas.

O DISM inclui um Shim para o Windows Vista SP1 e posterior, bem como para o Windows Server 2008 RTM e posterior, que redireciona as chamadas de pkgmgr de aplicativos herdados em execução no Windows 7 para o DISM. Se o aplicativo estiver em execução em um dos sistemas operacionais com suporte, o Shim roteará a chamada para Pkgmgr. Não existem correções para aplicativos herdados que chamam PEImg ou IntlConfg.

## <a name="usage"></a>Uso

O DISM é transparente para os usuários finais de pkgmgr em qualquer uma das plataformas com suporte. No entanto, se um aplicativo chamar o PEImg ou o IntlConfg do Windows 7, a chamada falhará.

Atualize todos os scripts que chamam pkgmgr, PEImg ou IntlConfg para chamar o DISM em vez disso. É importante incluir a atualização de scripts do pkgmgr nesse esforço, já que o Shim que fornece compatibilidade com versões anteriores para o pkgmgr será removido em versões futuras dos sistemas operacionais Windows.

Verifique se as chamadas para o DISM substituiram todas as chamadas para pkgmgr, PEImg e IntlConfg, e se a operação é executada com êxito.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciamento e manutenção de imagens de implantação (TechNet)](/previous-versions/windows/it-pro/windows-7/dd744256(v=ws.10))
</dt> </dl>

 

 
