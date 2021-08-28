---
title: Habilitando o rastreamento do EAPHost
description: O pode ajudar os usuários a encontrar as causas raiz dos problemas que ocorrem durante o processo de autenticação EAP. As informações de depuração podem incluir chamadas de API executadas, chamadas de função internas executadas e transições de estado executadas.
ms.assetid: 5f401101-59aa-4ee8-825a-0b998489eed9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c638fa7f546028cd9cf66227cfe3c302d6599492d1cbbfcfdac6c2b428273db8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086288"
---
# <a name="enabling-eaphost-tracing"></a>Habilitando o rastreamento do EAPHost

Os logs de rastreamento que contêm informações de depuração podem ajudar os usuários a encontrar as causas raiz dos problemas que ocorrem durante o processo de autenticação EAP. As informações de depuração podem incluir chamadas de API executadas, chamadas de função internas executadas e transições de estado executadas.

O rastreamento pode ser habilitado tanto no lado do cliente quanto no lado do autenticador. O rastreamento também pode ser habilitado para chamadas para as APIs [RRAS (serviço de roteamento e acesso remoto)](/windows/desktop/RRAS/routing-start-page) . Para obter mais informações, consulte [rastreamento no serviço de roteamento e acesso remoto](#tracing-on-the-routing-and-remote-access-service).

> [!Note]  
> Os logs de rastreamento estão disponíveis apenas em inglês.

 

Quando o rastreamento EAPHost está habilitado, as informações de log são armazenadas em um arquivo. etl em um local especificado pelo usuário. Se ocorrerem erros durante a autenticação EAP, o rastreamento gerará um arquivo. etl que pode ser enviado ao Microsoft Suporte Developer para análise da causa raiz. Os parceiros que têm acesso ao Microsoft Windows Build compartilhamentos, símbolos e arquivos traceformat podem converter os arquivos. etl em um arquivo de texto sem formatação usando a ferramenta **Tracerpt** .

Falhas de servidor de diretivas de rede (NPS) não são capturadas nos logs do EAPHost. Se você estiver tentando solucionar uma falha de NPS, exiba o IASSAM. LOG e [IASNAP. ](https://go.microsoft.com/fwlink/p/?linkid=84108) Arquivos de log.

## <a name="tracing-on-the-client"></a>Rastreamento no cliente

Para habilitar o rastreamento no lado do cliente:

1.  Abra uma janela de prompt de comando elevado.
2.  Execute o seguinte comando: **logman** **Start Trace** **EapHostPeer** **-o** **. \\ EapHostPeer. etl** **-p** **{5F31090B-D990-4e91-B16D-46121D0255AA} 0x4000ffff 0** **-ETS**
3.  Reproduza o cenário que você deseja rastrear.
4.  Execute o seguinte comando: **logman** **Stop** **EapHostPeer** **-ETS**
5.  Converta o arquivo ETL em texto usando o seguinte comando **: Tracerpt EapHostPeer. etl** **– PDB** **&lt; &gt; PDBPath** **-TP** **&lt; tracemessagefilesdirectorypath &gt;** **-o** **EapHostPeer.txt**
    > [!Note]  
    > Se você não tiver acesso à ferramenta tracerpt, evite a última etapa e envie o arquivo. ETL para o Microsoft Suporte Developer.

     

## <a name="tracing-on-the-authenticator"></a>Rastreamento no Authenticator

Para habilitar o rastreamento no lado do autenticador:

1.  Abra uma janela de prompt de comando elevado.
2.  Execute o seguinte comando: **logman** **Start Trace** **EapHostAuthr** **-o** **. \\ EapHostAuthr. etl** **-p** **{F6578502-DF4E-4A67-9661-E3A2F05D1D9B} 0x4000ffff 0** **-ETS**
3.  Reproduza o cenário que você deseja rastrear.
4.  Execute o seguinte comando: **logman** **Stop** **EapHostAuthr** **-ETS**
5.  Converta o arquivo ETL em texto usando o seguinte comando **: Tracerpt EapHostAuthr. etl** **– PDB** **&lt; &gt; PDBPath** **-TP** **&lt; tracemessagefilesdirectorypath &gt;** **-o** **EapHostAuthr.txt**
    > [!Note]  
    > Se você não tiver acesso à ferramenta tracerpt, evite a última etapa e, em vez disso, envie o arquivo. ETL para o Microsoft Suporte Developer.

     

## <a name="event-tracing"></a>Rastreamento de eventos

no Windows 7 e versões posteriores do Windows, o EapHost fornece rastreamento baseado em evento no autenticador e no par. A vantagem do rastreamento baseado em eventos é que nenhum arquivo de símbolo é necessário para exibir as mensagens de rastreamento. Para habilitar o rastreamento de eventos:

1.  Abra **Visualizador**.
2.  As mensagens importantes do EapHost são registradas em: "eventos administrativos de exibições personalizadas \\ "
3.  mensagens não críticas são registradas em: "aplicativos e serviços \\ Microsoft \\ Windows \\ EapHost
4.  As mensagens de evento "analítica" e "depurar" podem ser vistas no mesmo caminho selecionando **Mostrar logs analíticos e de depuração** no menu **Exibir** na barra de título.

## <a name="tracing-on-the-routing-and-remote-access-service"></a>Rastreamento no serviço de roteamento e acesso remoto

Para habilitar o rastreamento RRAS:

1.  Abra uma janela de prompt de comando elevado.
2.  Execute o seguinte comando: **netsh** **RAS** **set** **TR** **\* *_ _* en**
3.  Abrir o **\\ rastreamento de% systemroot%** para exibir os RASTREAMENTOs de Ras

Para desabilitar o rastreamento RRAS:

1.  Abra uma janela de prompt de comando elevado.
2.  Execute o seguinte comando: **netsh** **RAS** **set** **TR** **\* *_ _* dis**

Para obter mais informações, consulte [comandos netsh](/previous-versions/windows/it-pro/windows-server-2003/cc779693(v=ws.10)).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o EAPHost](using-eap-host.md)
</dt> <dt>

[Serviço de Roteamento e Acesso Remoto (RRAS)](/windows/desktop/RRAS/routing-start-page)
</dt> </dl>

 

 