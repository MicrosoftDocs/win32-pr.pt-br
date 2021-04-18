---
description: Não há mais suporte para os arquivos de log do WMI.
ms.assetid: 4ba80063-7aa6-42df-a620-1b366b795034
ms.tgt_platform: multiple
title: Registrando em log a atividade WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6ced8645eb7ad9005e6ba751d011ae7f0ccb3dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781354"
---
# <a name="logging-wmi-activity"></a>Registrando em log a atividade WMI

Não há mais suporte para os arquivos de log do WMI. A partir do Windows Vista, o WMI usa o [ETW (rastreamento de eventos para Windows](/windows/desktop/ETW/event-tracing-portal)) e eventos que estão disponíveis por meio da interface do usuário do **Visualizador de eventos** ou da ferramenta de linha de comando wevtutil. Para obter mais informações, consulte o provedor de ETW e a documentação de linha de comando do [wevutil](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc732848(v=ws.11)) .

As seções a seguir são discutidas neste tópico:

-   [Arquivos de log do WMI antes do Windows Vista](#wmi-log-files-before-windows-vista)
-   [Atividades de registro em log para componentes básicos do WMI antes do Windows Vista](#logging-activities-for-wmi-core-components-before-windows-vista)
-   [Atividades de registro em log para componentes do provedor de WMI antes do Windows Vista](#logging-activities-for-wmi-provider-components-before-windows-vista)
-   [Tópicos relacionados](#related-topics)

## <a name="wmi-log-files-before-windows-vista"></a>Arquivos de log do WMI antes do Windows Vista

Os arquivos de log criados pelo WMI e vários provedores registram: eventos, rastreamento ou dados de diagnóstico, erros e várias atividades. Somente os administradores têm acesso de leitura à pasta de log do WMI encontrada em% windir% \\ System32 \\ WBEM \\ logs.

Somente os componentes principais do WMI ou os provedores WMI gravam em arquivos de log. Você só pode ler ou exibir os dados nesses logs para fins de diagnóstico. Você pode criar e armazenar seus próprios arquivos de log no diretório de log do WMI.

## <a name="logging-activities-for-wmi-core-components-before-windows-vista"></a>Atividades de registro em log para componentes básicos do WMI antes do Windows Vista

Esses arquivos não contêm um formato consistente que seja adequado para leitura programaticamente. Para obter mais informações sobre logs específicos, consulte [arquivos de log do WMI](wmi-log-files.md).

As atividades de registro em log para componentes principais do WMI ocorrem quando as seguintes chaves do registro são definidas:

-   Nível de log

    As alterações no valor do registro de nível de log entram em vigor imediatamente. Nenhuma reinicialização do serviço WMI é necessária.

    **HKEY \_ SOFTWARE do \_ computador local** \\  \\ registro em log **do Microsoft** \\ **WBEM** \\ **CIMOM** \\  = 2

    A lista a seguir lista os níveis de log que podem ser definidos no registro.

    

    | Nível de log | Descrição               |
    |---------------|---------------------------|
    | 0             | Sem registro em log                |
    | 1             | Erros de log apenas           |
    | 2             | Log detalhado (padrão) |

    

     

-   Local do arquivo de log

    Para que as alterações no local do arquivo de log entrem em vigor, reinicie o serviço WMI.

    **HKEY \_ \_** Diretório de log do software do computador local \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **Directory** =% windir% \\ System32 \\ WBEM \\ logs

-   Tamanho máximo do arquivo de log, em bytes

    **HKEY \_ \_Computador local** \\ **software** \\ arquivo de log **do Microsoft** \\ **WBEM** \\ **CIMOM** \\ **tamanho máximo** = 65536

Você pode alterar esses valores de chave do registro por meio do editor do registro ou através do snap-in do WMI para o console de gerenciamento Microsoft.

**Para definir o nível de log para WMI antes do Windows Vista**

1.  Clique em **Iniciar** e em **Executar**.
2.  Digite **wmimgmt. msc**
3.  No menu **Ação**, clique em **Propriedades**.
4.  Na guia **registro em log** , defina o nível de log como **desabilitado**, **habilitado** ou **detalhado**.
5.  Em **local:**, digite o caminho para a pasta do arquivo de log e, em **tamanho máximo (bytes):**, defina o tamanho máximo, em bytes, do arquivo de log.

Para obter mais informações sobre como definir as propriedades do arquivo de log, consulte a ajuda online para o aplicativo controle WMI.

## <a name="logging-activities-for-wmi-provider-components-before-windows-vista"></a>Atividades de registro em log para componentes do provedor de WMI antes do Windows Vista

Quando o registro em log para componentes do WMI Core está habilitado, o log também é habilitado para qualquer provedor com recursos de log.

A lista a seguir lista os valores necessários.

<dl> <dt>

<span id="File"></span><span id="file"></span><span id="FILE"></span>**Grupo**
</dt> <dd>

Caminho completo e nome do arquivo de log. O valor padrão é% windir% \\ System32 \\ WBEM \\ logs. O **tipo** nomeado value deve ser definido como = File para que esse valor nomeado seja usado.

</dd> <dt>

<span id="Level"></span><span id="level"></span><span id="LEVEL"></span>**Geral**
</dt> <dd>

Uma máscara lógica de 32 bits que define o tipo de saída de depuração gerado pelo provedor. Esse valor é dependente do provedor. O valor padrão é 0 (zero).

</dd> <dt>

<span id="MaxFileSize"></span><span id="maxfilesize"></span><span id="MAXFILESIZE"></span>**Cedido**
</dt> <dd>

Tamanho máximo do arquivo, em bytes, do arquivo de log. Esse valor inteiro deve estar no intervalo de 1024 a 2 ^ 32-1. Quando o tamanho do arquivo exceder esse valor, o arquivo será renomeado para **~ filename** e um novo arquivo de log vazio será criado. O espaço em disco necessário para o arquivo de log é o dobro do valor de **MaxFileSize**. O valor padrão é 65.535.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Escreva**
</dt> <dd>

Pode ser definido como = File ou = Debugger. Se definido como = File, as informações de rastreamento serão gravadas no arquivo de log especificado no **arquivo** denominado Value. O valor padrão é = File.

</dd> </dl>

Por exemplo, para registrar consultas e obter chamadas de instância do provedor de exibição, use os valores de chave do registro a seguir. O log estará localizado na pasta de log e será o tamanho de arquivo padrão.

**HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **Providers** \\ **loggingprovider** \\  \\ **arquivo** = C: \\ Windows \\ System32 \\ WBEM \\ logs \\ viewprovider. log

**HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **provedores** \\ **logs** \\ **viewprovider** \\ **nível** = 2

**HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **provedores** \\ **logs** \\ **viewprovider** \\ **MaxFileSize** = 65535

**HKEY \_ SOFTWARE da \_ máquina local** \\ **softwares** \\ **Microsoft** \\ **WBEM** \\  \\ **logs** \\ **viewprovider** \\ **tipo** = arquivo

> [!Note]  
> Para seus próprios provedores com recursos de log, você precisa gravar as chaves e os valores necessários do registro para habilitar o registro em log.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Solução de problemas do WMI](wmi-troubleshooting.md)
</dt> <dt>

[Arquivos de log do WMI](wmi-log-files.md)
</dt> <dt>

[Classes de solução de problemas do WMI](wmi-troubleshooting-classes.md)
</dt> <dt>

[Rastreando a atividade WMI](tracing-wmi-activity.md)
</dt> </dl>

 

 
