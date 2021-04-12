---
title: Configurando SAP e RPC
description: Os servidores de rede Novell NetWare usam o SAP (Service Advertising Protocol) para transmitir informações sobre os serviços disponíveis na rede para outros dispositivos de rede.
ms.assetid: 6d6ef481-fc09-4795-8954-33329912ff4f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 385d60168a52cbe5d31368959ec4f21d52f9ad80
ms.sourcegitcommit: 1e8e6e6f27c909900cfa8be58b042456331a82ad
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/15/2019
ms.locfileid: "104364528"
---
# <a name="configuring-sap-and-rpc"></a>Configurando SAP e RPC

Os servidores de rede Novell NetWare usam o SAP (Service Advertising Protocol) para transmitir informações sobre os serviços disponíveis na rede para outros dispositivos de rede. Um servidor pode enviar uma difusão SAP a cada 60 segundos para informar outros dispositivos de rede sobre os serviços que ele oferece. As estações de trabalho usam SAPs para encontrar os serviços de que precisam na rede.

O Windows inclui um serviço de Agente SAP para permitir que servidores baseados no Windows interajam com servidores NetWare. O serviço do Agente SAP escutará as solicitações SAP dos clientes de rede para serviços baseados em IPX que estão instalados e em execução no servidor.

O software que foi projetado para ser anunciado como um serviço pela rede por meio de uma difusão SAP emitirá anúncios SAP a cada 60 segundos, sem ter o Agente SAP instalado. No entanto, para que os clientes de rede localizem rapidamente um serviço de rede IPX, um servidor que mantém um banco de dados de serviço deve estar disponível na rede para responder à solicitação de local de serviço. Esse banco de dados de serviço geralmente é mantido por um Novell NetWare ou por um servidor compatível com NetWare. Os serviços de arquivo e impressão da Microsoft para NetWare também manterão um banco de dados de serviço de rede IPX.

Em um computador executando o Windows Server, se os serviços de gateway para NetWare (GSNW) estiverem instalados, um tipo SAP 640 transmitirá a cada 60 segundos pelo serviço RPC (chamada de procedimento remoto). Essa difusão SAP continuará mesmo se o usuário desabilitar o GSNW e o serviço do Agente SAP.

O serviço RPC fará a difusão do SAP se os serviços cliente para NetWare (CSNW) e o serviço do Agente SAP estiverem instalados. Essa difusão SAP continuará mesmo se o usuário desabilitar o Agente SAP.

Por padrão, o serviço RPC verificará a presença de serviços de gateway para NetWare e o serviço de Agente SAP no computador que executa o Windows Server. A instalação dos serviços de arquivo e impressão para NetWare instala um agente SAP.

No computador que executa uma versão cliente do Windows com o CSNW, o serviço RPC verifica o serviço do Agente SAP. Se os serviços estiverem presentes, o RPC iniciará seu próprio thread que fará o tipo de difusão SAP 640 a cada minuto.

> [!NOTE]
> Se você não quiser difusões do SAP na rede a cada 60 segundos, poderá desabilitar difusões do SAP usando o editor do registro. Seja avisado de que o uso incorreto do editor do registro pode causar sérios problemas que podem exigir a reinstalação do sistema operacional. A Microsoft não garante que problemas resultantes do uso incorreto do Editor do Registro possam ser solucionados. Use o Editor do Registro por sua conta e risco. Você deve fazer backup do registro antes de editá-lo.

 

**Para configurar o para SAP**

1.  Execute o editor do registro (Regedt32.exe) e vá para a seguinte chave no registro:

    **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ RPC**

2.  No menu **Editar** , clique em **adicionar valor** e use a seguinte entrada:
    1.  Nome do valor: AdvertiseRpcService
    2.  Tipo de dados: REG \_ sz
    3.  Cadeia de caracteres: não
3.  Usar não para a cadeia de caracteres transforma a difusão RPC SAP off. Usar Sim para a cadeia de caracteres ativa a difusão RPC SAP.
4.  Reinicie o computador para que a alteração do registro entre em vigor.
    > [!NOTE]
    > Se as difusões do SAP continuarem depois de seguir essas etapas, talvez você queira tentar uma etapa de solução de problemas. Exclua o valor da cadeia de caracteres **ncacn \_ SPX** na seguinte chave do registro:
    >
    > **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ RPC \\ ServerProtocols\\**

     

> [!NOTE]  
> Isso deve ser usado apenas como uma etapa de solução de problemas. A exclusão desse valor de cadeia de caracteres desabilita completamente as difusões do SAP que alguns programas podem precisar para funcionar corretamente.