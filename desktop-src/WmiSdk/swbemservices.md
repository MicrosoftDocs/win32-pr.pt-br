---
description: Você pode usar os métodos de um objeto SWbemServices para executar operações em um namespace em um host local ou em um host remoto. Este objeto não pode ser criado pela chamada VBScript CreateObject.
ms.assetid: 7fcfa404-2fe6-42e5-85ac-64536f6d2a44
ms.tgt_platform: multiple
title: Objeto SWbemServices (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices
- ISWbemServices
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4303b3226acc6d773ed35e77176e05e3a58c567d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811716"
---
# <a name="swbemservices-object"></a>Objeto SWbemServices

Você pode usar os métodos de um objeto **SWbemServices** para executar operações em um namespace em um host local ou em um host remoto. Este objeto não pode ser criado pela chamada VBScript **CreateObject** .

## <a name="members"></a>Membros

O objeto **SWbemServices** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **SWbemServices** tem esses métodos.



| Método                                                                         | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AssociatorsOf**](swbemservices-associatorsof.md)                           | Recupera as instâncias de recursos gerenciados que estão associados a um recurso especificado por meio de uma ou mais classes de associação. Você fornece o caminho do objeto para o ponto de extremidade de origem e [**AssociatorsOf**](swbemservices-associatorsof.md) retorna os recursos gerenciados no ponto de extremidade oposto. O método **AssociatorsOf** executa a mesma função que a consulta WQL "ASSOCIATORS of" executa.<br/>                                                                           |
| [**AssociatorsOfAsync**](swbemservices-associatorsofasync.md)                 | De forma assíncrona retorna uma coleção de objetos (classes ou instâncias) que estão associados a um objeto especificado.<br/>                                                                                                                                                                                                                                                                                                                                                                             |
| [**Apagar**](swbemservices-delete.md)                                         | Exclui uma instância de um recurso gerenciado (ou uma definição de classe do repositório CIM).<br/>                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**DeleteAsync**](swbemservices-deleteasync.md)                               | Exclui de forma assíncrona a classe ou instância especificada no caminho do objeto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**ExecMethod**](swbemservices-execmethod.md)                                 | Fornece uma maneira alternativa para executar um método definido por uma definição de classe de recurso gerenciado. Usado principalmente em situações em que a linguagem de script não dá suporte a parâmetros de saída. Por exemplo, o JScript não dá suporte a parâmetros de saída.<br/>                                                                                                                                                                                                                                            |
| [**ExecMethodAsync**](swbemservices-execmethodasync.md)                       | Executa de forma assíncrona um método que é exportado por um provedor de método.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**ExecNotificationQuery**](swbemservices-execnotificationquery.md)           | Executa uma consulta de assinatura de evento para receber eventos. Uma consulta de assinatura de evento é uma consulta que define uma alteração no ambiente gerenciado que você deseja monitorar. Quando a alteração ocorre, a infraestrutura do WMI fornece um evento que descreve a alteração no script de chamada.<br/>                                                                                                                                                                                                        |
| [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) | Executa de forma assíncrona uma consulta para receber eventos.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**ExecQuery**](swbemservices-execquery.md)                                   | Executa uma consulta para recuperar uma coleção de instâncias de recursos gerenciados por WMI (ou definições de classe). [**ExecQuery**](swbemservices-execquery.md) pode ser usado para recuperar uma coleção filtrada de instâncias que correspondem aos critérios que você define na consulta passada para **ExecQuery**.<br/>                                                                                                                                                                                                           |
| [**ExecQueryAsync**](swbemservices-execqueryasync.md)                         | Executa de forma assíncrona uma consulta para recuperar objetos.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**Obter**](swbemservices-get.md)                                               | Recupera uma única instância de um recurso gerenciado (ou definição de classe) com base em um caminho de objeto.<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| [**Getasync**](swbemservices-getasync.md)                                     | Recupera de forma assíncrona um objeto, que é uma definição de classe ou uma instância, com base no caminho do objeto.<br/>                                                                                                                                                                                                                                                                                                                                                                                |
| [**InstancesOf**](swbemservices-instancesof.md)                               | Recupera todas as instâncias de um recurso gerenciado com base em um nome de classe. Por padrão, o [**InstancesOf**](swbemservices-instancesof.md) executa uma recuperação profunda. Ou seja, **InstancesOf** recupera as instâncias do recurso identificado pelo nome de classe passado para o método e também recupera todas as instâncias de todos os recursos que são subclasses (definidos abaixo) da classe de destino.<br/>                                                                                       |
| [**InstancesOfAsync**](swbemservices-instancesofasync.md)                     | Retorna de forma assíncrona as instâncias de uma classe especificada de acordo com os critérios de seleção especificados pelo usuário.<br/>                                                                                                                                                                                                                                                                                                                                                                                  |
| [**Referências a**](swbemservices-referencesto.md)                             | Retorna todas as associações que fazem referência a um recurso especificado. A melhor maneira de entender [**referênciasto**](swbemservices-referencesto.md) é compará-la com o método [**AssociatorsOf**](swbemservices-associatorsof.md) . **AssociatorsOf** retorna os recursos dinâmicos que estão na extremidade oposta de uma associação. **References** para retorna a associação em si. O método **References** executa a mesma função que as "referências de" consulta WQL executa.<br/> |
| [**ReferencesToAsync**](swbemservices-referencesto.md)                        | Retorna de forma assíncrona uma coleção de todas as classes ou instâncias de associação que se referem a uma classe ou instância específica.<br/>                                                                                                                                                                                                                                                                                                                                                                        |
| [**SubclassesOf**](swbemservices-subclassesof.md)                             | Recupera todas as subclasses de uma classe especificada do repositório CIM.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**SubclassesOfAsync**](swbemservices-subclassesofasync.md)                   | De forma assíncrona retorna uma coleção de subclasses para uma classe especificada.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |



 

### <a name="properties"></a>Propriedades

O objeto **SWbemServices** tem essas propriedades.



| Propriedade                                                 | Tipo de acesso          | Descrição                                                                          |
|:---------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------|
| [**Segurança\_**](swbemservices-security-.md)<br/> | Somente leitura<br/> | Usado para obter ou definir as configurações de segurança para um objeto **SWbemServices** .<br/> |



 

## <a name="remarks"></a>Comentários

Os métodos podem ser chamados no modo síncrono, no modo assíncrono ou no modo semisynchronous. Para obter mais informações, consulte [chamando um método](calling-a-method.md).

**Visão geral**

**SWbemServices** atende a duas funções principais. Primeiro, o objeto **SWbemServices** representa uma conexão autenticada a um namespace WMI em um computador de destino. Em segundo lugar, **SWbemServices** é o objeto de automação que você usa para recuperar recursos gerenciados por WMI. Você pode obter uma referência a um objeto **SWbemServices** de uma das duas maneiras:

-   Conforme demonstrado na maioria dos scripts WMI apresentados até agora, você pode usar a função VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) em combinação com o moniker WMI "winmgmts:". O exemplo a seguir é a forma mais simples de uma conexão WMI. O exemplo se conecta ao namespace padrão (normalmente "raiz \\ CIMv2") no computador local:

    `Set objSWbemServices = GetObject("winmgmts:")`

-   Você também pode usar o método [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) do objeto [**SWbemLocator**](swbemlocator.md) para obter uma referência a um objeto **SWbemServices** .

Depois de obter uma referência a um objeto **SWbemServices** , use a referência de objeto para chamar 1 de 18 métodos disponíveis usando **SWbemServices**. **SWbemServices** pode retornar um dos três objetos de biblioteca de script WMI diferentes ([**SWbemObjectSet**](swbemobjectset.md), [**SWbemObject**](swbemobject.md)ou [**SWbemEventSource**](swbemeventsource.md)), dependendo do método que você chama. Saber o tipo de objeto que cada método retorna ajudará a determinar a próxima etapa que seu script deve tomar. Por exemplo, se você retornar um **SWbemObjectSet**, deverá enumerar a coleção para acessar cada **SWbemObject** na coleção. Se você retornar um **SWbemObject**, poderá acessar imediatamente os métodos e as propriedades do objeto sem enumerar a coleção primeiro.

**Modos de operação**

O **SWbemServices** dá suporte a três modos de operação: síncrono, assíncrono e semisynchronous.

-   **Síncrono**. No modo síncrono, seu script bloqueia (pausa) até que o método **SWbemServices** seja concluído. Não apenas a espera do seu script, mas em casos em que o WMI recupera instâncias de recursos gerenciados, o WMI cria o [**SWbemObjectSet**](swbemobjectset.md) inteiro na memória antes que o primeiro byte de dados seja retornado para o script de chamada. Isso pode ter um efeito adverso no desempenho do script e no computador que executa o script. Por exemplo, a recuperação síncrona de milhares de eventos dos logs de eventos do Windows pode levar muito tempo e usar muita memória. Por esses motivos, as operações síncronas não são recomendadas, exceto para os três métodos ([**delete**](swbemservices-delete.md), [**ExecMethod**](swbemservices-execmethod.md)e [**Get**](swbemservices-get.md)) que são síncronos por padrão. Esses métodos não retornam grandes conjuntos de dados, portanto, a operação semisynchronous não é necessária.
-   **Assíncrono**. No modo assíncrono, seu script chama um dos nove métodos assíncronos e retorna imediatamente. Ou seja, assim que o método assíncrono for chamado, o script retomará a execução da próxima linha de código. Para usar um método assíncrono, o script deve primeiro criar um objeto [**SWbemSink**](swbemsink.md) e uma sub-rotina especial chamada manipulador de eventos. O WMI executa a operação assíncrona e notifica o script chamando a sub-rotina do manipulador de eventos quando a operação é concluída.
-   **Semisynchronous**. O modo Semisynchronous é um comprometimento entre síncrono e assíncrono. As operações Semisynchronous oferecem melhor desempenho do que as operações síncronas, ainda que não exijam o conhecimento extra e as etapas de script necessárias para lidar com operações assíncronas. Esse é o tipo de operação padrão para a maioria das consultas WMI.

    No modo semisynchronous, seu script chama um dos seis métodos de recuperação de dados e retorna imediatamente. O WMI recupera os recursos gerenciados em segundo plano à medida que o script continua a ser executado. À medida que os recursos são recuperados, eles são retornados imediatamente para o script por meio de um SWbemObjectSet. Você pode começar a acessar os recursos gerenciados sem esperar que toda a coleção seja montada.

    Há uma limitação para semisynchronous operações quando você está trabalhando com recursos gerenciados que têm muitas instâncias (muitos significando mais de 1.000), como [**CIM \_ DataFile**](/windows/desktop/CIMWin32Prov/cim-datafile) e [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent). A limitação é um resultado de como o WMI lida com instâncias de recursos gerenciados. Para cada instância de um recurso gerenciado, o WMI cria e armazena em cache um objeto [**SWbemObject**](swbemobject.md) . Quando há um grande número de instâncias para um recurso gerenciado, a recuperação da instância pode monopolizar os recursos disponíveis, reduzindo o desempenho do script e do computador.

    Para contornar o problema, você pode otimizar as chamadas de método semisynchronous usando o sinalizador **wbemFlagForwardOnly** . O sinalizador **wbemFlagForwardOnly** , combinado com o sinalizador **wbemFlagReturnImmediately** (o sinalizador semisynchronous padrão), informa ao WMI para retornar um [**SWbemObjectSet**](swbemobjectset.md)somente de encaminhamento, o que elimina o grande problema de desempenho do conjunto de dados. No entanto, o uso do sinalizador **wbemFlagForwardOnly** vem com um custo. Um **SWbemObjectSet** somente de encaminhamento pode ser enumerado apenas uma vez. Depois que cada [**SWbemObject**](swbemobject.md) em um **SWbemObjectSet** somente de encaminhamento for acessado, a memória alocada para a instância será liberada.

Com exceção dos métodos assíncronos [**delete**](swbemservices-delete.md), [**ExecMethod**](swbemservices-execmethod.md), [**Get**](swbemservices-get.md)e nove, semisynchronous é o modo de operação padrão e recomendado.

**Métodos comumente usados**

Os métodos usados com mais frequência nos scripts de administração do sistema são [**InstancesOf**](swbemservices-instancesof.md), [**ExecQuery**](swbemservices-execquery.md), [**Get**](swbemservices-get.md)e [**ExecNotificationQuery**](swbemservices-execnotificationquery.md). Embora seja usado com frequência, o **InstancesOf** não é necessariamente a maneira recomendada de recuperar informações (embora seja, de forma imprecisa, a maneira mais fácil).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMSERVICES CLSID<br/>                                                         |
| IID<br/>                      | ISWbemServices de IID \_<br/>                                                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de API de script](scripting-api-objects.md)
</dt> <dt>

[Chamando um método](calling-a-method.md)
</dt> </dl>

 

