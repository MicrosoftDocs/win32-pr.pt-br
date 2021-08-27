---
title: Usando extensões NPS
description: Saiba mais sobre como usar extensões NPS. O IAS (Serviço de Autenticação da Internet) foi renomeado como NPS (Servidor de Políticas de Rede).
ms.assetid: 3ee16279-7e11-4587-ae43-f0296b7e7594
ms.tgt_platform: multiple
keywords:
- IAS do Serviço de Autenticação da Internet, tarefas
- IAS do Serviço de Autenticação da Internet, usando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4db3590ed10ec77e57c86bfad3e0e0b1160e70a2d6fcc08abc911a14614543f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074296"
---
# <a name="using-nps-extensions"></a>Usando extensões NPS

O IAS (Serviço de Autenticação da Internet) foi renomeado como NPS (Servidor de Políticas de Rede). O conteúdo deste tópico se aplica a IAS e NPS. Em todo o texto, o NPS é usado para se referir a todas as versões do serviço, incluindo as versões originalmente conhecidas como IAS.

**Windows Server 2008 R2 e Windows Server 2008: **

Os exemplos DialIn e MapName estendem a funcionalidade NPS.



| Amostra             | Descrição                                                                                                                                                                                                     |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dialin<br/>  | Este exemplo implementa uma DLL de extensão RADIUS que verifica o bit discado do usuário.<br/>                                                                                                              |
| Mapname<br/> | Esta DLL de extensão de exemplo pesquisa todos os domínios confiáveis para a conta designada. Isso permite que os usuários de vários domínios sejam autenticados sem que os usuários sejam obrigados a fornecer seu nome de domínio.<br/> |



 

Você pode encontrar o código-fonte para os aplicativos de exemplo MapName e DialIn na lista a seguir. *Location*, %Install Path%, designa o diretório de instalação base para computadores x64. Consulte também [Windows SDK (Software Development Kit)](https://developer.microsoft.com/windows/downloads/windows-8-sdk)para Windows 8 , SDK (Software Development Kit) da Microsoft Windows e Downloads para desenvolvimento de aplicativos da [Windows Store.](https://msdn.microsoft.com/windows/apps/br229516)

<dl> <dt>

Windows SDK para Windows 8
</dt> <dd>

Windows Server 2012

Link de download: N/A

MapName: Não

DialIn: Não

Local: N/A

</dd> <dt>

Microsoft Windows SDK (Software Development Kit) para Windows 7 e .NET Framework 4.0
</dt> <dd>

Windows Server 2008 R2

Link de download: <https://www.microsoft.com/download/en/confirmation.aspx?id=8279>

MapName: Sim

DialIn: Não

Local: %Install Path% \\ Microsoft SDKs \\ Windows \\ v7.1 \\ Exemplos \\ netds \\ ias

</dd> <dt>

SDK do Windows
</dt> <dd>

Windows Server 2008

Link de download: <https://www.microsoft.com/download/details.aspx?id=5023>

MapName: Sim

DialIn: Não

Local: %Install Path% \\ Microsoft SDKs \\ Windows \\ v6.1 \\ \\ Samples NetDs \\ IAS

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Downloads para desenvolvedores](https://msdn.microsoft.com/windows/apps/br229516)
</dt> <dt>

[Windows SDK para Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk)
</dt> </dl>

 

 





