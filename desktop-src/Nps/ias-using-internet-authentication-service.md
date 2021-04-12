---
title: Usando extensões do NPS
description: O IAS (serviço de autenticação da Internet) foi renomeado como NPS (servidor de políticas de rede).
ms.assetid: 3ee16279-7e11-4587-ae43-f0296b7e7594
ms.tgt_platform: multiple
keywords:
- IAS, tarefas do serviço de autenticação da Internet
- Serviço de autenticação da Internet IAS, usando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a1cc9f10c810ec9fe16618144db11686a1e2132
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2020
ms.locfileid: "104499008"
---
# <a name="using-nps-extensions"></a>Usando extensões do NPS

O IAS (serviço de autenticação da Internet) foi renomeado como NPS (servidor de políticas de rede). O conteúdo deste tópico aplica-se ao IAS e ao NPS. Em todo o texto, o NPS é usado para fazer referência a todas as versões do serviço, incluindo as versões originalmente chamadas de IAS.

* * Windows Server 2008 R2 e Windows Server 2008: * *

Os exemplos de Diale e MapName estendem a funcionalidade do NPS.



| Amostra             | Descrição                                                                                                                                                                                                     |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Conexão<br/>  | Este exemplo implementa uma extensão RADIUS DLL que verifica o bit de discagem para o usuário.<br/>                                                                                                              |
| MapName<br/> | Esta DLL de extensão de exemplo pesquisa todos os domínios confiáveis para a conta designada. Isso permite que os usuários de vários domínios sejam autenticados sem que os usuários precisem fornecer seu nome de domínio.<br/> |



 

Você pode encontrar o código-fonte para os aplicativos de exemplo MapName e dial-in na lista a seguir. *Local*,% caminho de instalação%, designa o diretório de instalação base para computadores x64. Consulte também [Windows Software Development Kit (SDK) para Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk), SDK (Software Development Kit) do Microsoft Windows e [downloads para o desenvolvimento de aplicativos da Windows Store](https://msdn.microsoft.com/windows/apps/br229516).

<dl> <dt>

SDK do Windows para Windows 8
</dt> <dd>

Windows Server 2012

Link de download: N/A

MapName: não

Conexão: não

Local: N/A

</dd> <dt>

SDK (Software Development Kit) do Microsoft Windows para Windows 7 e .NET Framework 4,0
</dt> <dd>

Windows Server 2008 R2

Link de download: <https://www.microsoft.com/download/en/confirmation.aspx?id=8279>

MapName: Sim

Conexão: não

Local:% Install caminho% \\ Microsoft SDKs \\ Windows \\ v 7.1 \\ Samples \\ netds \\ ias

</dd> <dt>

SDK do Windows
</dt> <dd>

Windows Server 2008

Link de download: <https://www.microsoft.com/download/details.aspx?id=5023>

MapName: Sim

Conexão: não

Local:% Install caminho% \\ Microsoft SDKs \\ Windows \\ v 6.1 \\ Samples \\ NetDs \\ ias

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Downloads para desenvolvedores](https://msdn.microsoft.com/windows/apps/br229516)
</dt> <dt>

[SDK do Windows para Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk)
</dt> </dl>

 

 





