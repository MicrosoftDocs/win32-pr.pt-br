---
description: As enumerações tendem a usar uma quantidade significativa de recursos do sistema.
ms.assetid: 4163e6c2-4ee3-4906-b297-618509666c90
ms.tgt_platform: multiple
title: Melhorando o desempenho da enumeração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df2554e9e1df2f2ece58f5703d6099d84acbe01c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170611"
---
# <a name="improving-enumeration-performance"></a>Melhorando o desempenho da enumeração

As enumerações tendem a usar uma quantidade significativa de recursos do sistema. Portanto, você deve tentar otimizar o processo de enumeração do WMI se planeja executar enumerações em um grupo grande. Os scripts também podem usar uma consulta para evitar a degradação do desempenho nas operações "for each.... Next" com um conjunto grande. Para obter mais informações, consulte [consultando o WMI](querying-wmi.md).

O procedimento a seguir descreve como melhorar o desempenho de enumeração.

**Para melhorar o desempenho de enumeração**

1.  Defina o parâmetro *lFlags* para permitir o retorno de semisynchronous dos dados com um enumerador que descarta cada item do WMI à medida que ele é entregue. Para obter mais informações, consulte [chamando um método](calling-a-method.md).

    O exemplo de código C++ a seguir mostra como usar **o \_ sinalizador WBEM \_ retornar sinalizadores \_ imediatos** e de **\_ \_ \_ somente encaminhamento do sinalizador WBEM** .

    `WBEM_FLAG_RETURN_IMMEDIATE | WBEM_FLAG_FORWARD_ONLY`

    No VBScript ou Visual Basic, use os sinalizadores de script **WbemFlagReturnImmediately** e **WbemFlagForwardOnly** do [WbemFlagEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum). O valor combinado desses sinalizadores é decimal 48.

    Os sinalizadores de script e de parâmetro causam o seguinte comportamento:

    -   O **\_ sinalizador WBEM \_ retorna \_** o comportamento de semisynchronous imediato ou **wbemFlagReturnImmediately** sinalizador de solicitação. A chamada para criar o enumerador retorna imediatamente. Em seguida, você pode começar a atravessar o conjunto de objetos que receber.
    -   O sinalizador de **\_ \_ \_ somente encaminhamento** do sinalizador WBEM ou sinalizador **wbemFlagForwardOnly** solicita um enumerador que você não pode retroceder. Ou seja, o WMI pode liberar um objeto depois de exibir o objeto.

    Em situações em que a enumeração é grande e o aplicativo é muito rápido, o uso de enumeradores somente de encaminhamento com processamento semisynchronous permite que o WMI mantenha um número muito menor de objetos, aumentando significativamente o tempo de resposta e o desempenho da memória.

    O exemplo de código VBScript a seguir mostra como fazer uma chamada usando os sinalizadores **wbemFlagReturnImmediately** e **wbemFlagForwardOnly** combinados para obter uma coleção de eventos de um log de eventos.

    ```VB
    Set Events = GetObject("winmgmts:").ExecQuery _
         ("SELECT * FROM Win32_NTLogEvent " _
          & "WHERE Logfile = 'System'",,48)
    ```

    

2.  Sempre que possível, evite usar o [**CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) em C++ ou [**SWbemServices. InstancesOf**](swbemservices-instancesof.md)e, em vez disso, use **ExecQuery**.

    O método **ExecQuery** consulta o WMI usando tecnologias de banco de dados, enquanto o [**CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) ou [**SWBEMSERVICES. InstancesOf**](swbemservices-instancesof.md) enumera objetos WMI. Especificamente, o **ExecQuery** pode solicitar subconjuntos específicos de dados que os métodos de enumeração não podem.

    Como alguns provedores não têm recursos de consulta, o WMI fornece um recurso de "post Filter" que permite ao WMI descartar instâncias que não atendam às especificações de uma consulta. Se um provedor específico se beneficia desse recurso, ele é o autor do provedor.

3.  Experimente consultas diferentes para determinar o que oferece o melhor desempenho.

    Por exemplo, o WMI raramente processa consultas com cláusulas **Where** no formato Prop1 < "x". Por outro lado, o WMI normalmente processa consultas no formato KeyProp1 = "x" com eficiência.

Para obter mais informações, consulte [enumerando o WMI](enumerating-wmi.md).

 

 



