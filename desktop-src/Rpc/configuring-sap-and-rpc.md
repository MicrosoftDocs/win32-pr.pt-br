---
title: Configurando SAP e RPC
description: Os servidores de rede Da Novell NetWare usam o PROTOCOLO SAP para transmitir informações sobre os serviços disponíveis na rede para outros dispositivos em rede.
ms.assetid: 6d6ef481-fc09-4795-8954-33329912ff4f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cf75a9ab45e97a66f1fc8d796b1d288367bb1c8d0e04b2ace4a90de7e21cbbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931679"
---
# <a name="configuring-sap-and-rpc"></a>Configurando SAP e RPC

Os servidores de rede Da Novell NetWare usam o PROTOCOLO SAP para transmitir informações sobre os serviços disponíveis na rede para outros dispositivos em rede. Um servidor pode enviar uma transmissão SAP a cada 60 segundos para informar outros dispositivos de rede sobre os serviços que ele oferece. As estações de trabalho usam SAPs para encontrar serviços de que precisam na rede.

Windows inclui um serviço do Agente SAP para permitir que Windows servidores baseados em dados interajam com servidores NetWare. O serviço agente SAP escutará as solicitações sap de clientes de rede para serviços baseados em IPX instalados e em execução no servidor.

O software projetado para ser anunciado como um serviço pela rede por meio de uma difusão SAP emitirá os comunicados sap a cada 60 segundos, sem ter o AGENTE SAP instalado. No entanto, para que os clientes de rede localizem rapidamente um serviço de rede IPX, um servidor que mantém um banco de dados de serviço deve estar disponível na rede para responder à solicitação de local do serviço. Esse banco de dados de serviço geralmente é mantido por um NetWare da Novell ou por um servidor compatível com NetWare. Os Serviços de Arquivo e Impressão da Microsoft para NetWare também manterão um banco de dados de serviço de rede IPX.

Em um computador que executa o Windows Server, se o Gateway Services for NetWare (GSNW) estiver instalado, um SAP Type 640 será transmitido a cada 60 segundos pelo serviço RPC (chamada de procedimento remoto). Essa difusão SAP continuará mesmo que o usuário desabilite o GSNW e o Serviço de Agente SAP.

O serviço RPC fará a difusão do SAP se os Serviços cliente para NetWare (CSNW) e o serviço agente SAP estão instalados. Essa difusão SAP continuará mesmo que o usuário desabilite o agente SAP.

Por padrão, o serviço RPC verificará a presença dos Serviços de Gateway para NetWare e do serviço sap Agent no computador que executa Windows Server. A instalação dos serviços de Arquivo e Impressão para NetWare instala um agente SAP.

No computador que executa uma versão de cliente do Windows com CSNW, o serviço RPC verifica o serviço agente SAP. Se os serviços estão presentes, o RPC iniciará seu próprio thread que fará o Tipo de difusão SAP 640 a cada minuto.

> [!NOTE]
> Se você não quiser transmissões SAP na rede a cada 60 segundos, poderá desabilitar as transmissões SAP usando o Editor do Registro. Seja avisado de que usar o Editor do Registro incorretamente pode causar problemas sérios que podem exigir que você reinstale seu sistema operacional. A Microsoft não garante que problemas resultantes do uso incorreto do Editor do Registro possam ser solucionados. Use o Editor do Registro por sua conta e risco. Você deve fazer o back-up do Registro antes de editá-lo.

 

**Para configurar para SAP**

1.  Execute o Editor do Registro (Regedt32.exe) e vá para a seguinte chave no Registro:

    **HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ RPC**

2.  No menu **Editar,** clique **em Adicionar Valor** e use a seguinte entrada:
    1.  Nome do valor: AdvertiseRpcService
    2.  Tipo de dados: REG \_ SZ
    3.  Cadeia de caracteres: Não
3.  Usar Não para a cadeia de caracteres desliga a difusão RPC SAP. Usar Sim para a cadeia de caracteres liga a difusão RPC SAP.
4.  Reinicie o computador para que a alteração do Registro entre em vigor.
    > [!NOTE]
    > Se as transmissões SAP continuarem após seguir essas etapas, talvez você queira tentar uma etapa de solução de problemas. Exclua o valor da cadeia **\_ de caracteres Ncacn spx** na seguinte chave do Registro:
    >
    > **HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Rpc \\ ServerProtocols\\**

     

> [!NOTE]  
> Isso deve ser usado apenas como uma etapa de solução de problemas. Excluir esse valor de cadeia de caracteres desabilita completamente as transmissões SAP das quais alguns programas podem precisar para funcionar corretamente.