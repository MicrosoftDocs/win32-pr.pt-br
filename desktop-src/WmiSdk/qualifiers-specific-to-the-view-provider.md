---
description: O a seguir lista os qualificadores usam para definir as classes do provedor de exibição.
ms.assetid: 31a6af2d-33da-44f2-86d7-c467dd2f3e00
ms.tgt_platform: multiple
title: Qualificadores específicos para o provedor de exibição
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers
api_type:
- NA
api_location: ''
ms.openlocfilehash: 76f28e4ba3433c168e1d0bf86887ee93df953444
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170887"
---
# <a name="qualifiers-specific-to-the-view-provider"></a>Qualificadores específicos para o provedor de exibição

O a seguir lista os qualificadores usam para definir as classes do provedor de exibição.

> [!Note]  
> A classe View Provider dá suporte apenas a nomes NetBIOS ao usar referências remotas. Se você usar um endereço IP ou um nome DNS em uma referência remota, a conexão falhará com um erro 0x800706BA.

 

<dt>

<span id="Direct"></span><span id="direct"></span><span id="DIRECT"></span>**Encaminhe**
</dt> <dd>

Tipo de dados: **booliano**

Usado com propriedades de associação de exibição para impedir que referências de associação sejam mapeadas para uma referência de exibição.

O exemplo a seguir define a propriedade **GroupComponent** como uma referência de associação que não está mapeada na referência de exibição.


```mof
[Direct, key, PropertySources
{"GroupComponent"}]
```



</dd> <dt>

<span id="HiddenDefault"></span><span id="hiddendefault"></span><span id="HIDDENDEFAULT"></span>**HiddenDefault**
</dt> <dd>

Tipo de dados: **booliano**

Valor padrão para uma propriedade de classe de exibição baseada em uma propriedade de classe de origem com um valor padrão diferente. A classe de origem subjacente é implícita pela exibição.

Por exemplo, a classe de origem [**Win32 \_ ScheduledJob**](/windows/desktop/CIMWin32Prov/win32-scheduledjob) tem uma propriedade [booleana](boolean.md) **RunRepeatedly** que indica se o trabalho deve ser executado periodicamente ou apenas uma vez. O valor padrão de **RunRepeatedly** não é verdadeiro para o **Win32 \_ ScheduledJob**, mas é verdadeiro para a classe de exibição.


```mof
#pragma namespace("\\\\.\\root\\ns_view")
[Union,
ViewSources{"select * from Win32_ScheduledJob where RunRepeatedly=True"},
ViewSpaces{"\\\\.\\root\\cimv2"},
dynamic,provider("MS_VIEW_INSTANCE_PROVIDER")]
Class View_PeriodicJob
{
 [key, PropertySources{"JobId"}]
 uint32 JobId;
 [PropertySources{"Command"}]
 string Command;
 [HiddenDefault,PropertySources{"RunRepeatedly"}]
 boolean Repeat = True;
};
```



</dd> <dt>

<span id="JoinOn"></span><span id="joinon"></span><span id="JOINON"></span>**Junção**
</dt> <dd>

Tipo de dados: **cadeia de caracteres**

Define como as instâncias de classe de origem são unidas em classes de exibição de junção. O exemplo a seguir mostra como usar o qualificador **Join** para unir duas classes de origem.


```mof
JoinOn("Win32Perf_RawProcess.IDProcess = Win32Perf_RawThread.IDProcess")
```



</dd> <dt>

<span id="MethodSource"></span><span id="methodsource"></span><span id="METHODSOURCE"></span>**Método**
</dt> <dd>

Tipo de dados: **matriz de cadeia de caracteres**

Método de origem a ser executado para o método de exibição. Para obter uma sintaxe semelhante, consulte [qualificador PropertySources](propertysources-qualifier.md). A assinatura do método deve corresponder exatamente à assinatura da classe de origem. Copie a assinatura do método do arquivo MOF que define a classe de origem. O exemplo a seguir define um método do método [**ClearEventLog**](/previous-versions/windows/desktop/eventlogprov/cleareventlog-method-in-class-win32-nteventlogfile) do [**Win32 \_ NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)):


```mof
[implemented, MethodSource
{"ClearEventlog"}]
  uint32   VClearEventlog([in] string ArchiveFileName);
```



Este qualificador só é válido quando é usado com exibições de União.

</dd> <dt>

<span id="PostJoinFilter"></span><span id="postjoinfilter"></span><span id="POSTJOINFILTER"></span>[**PostJoinFilter**](postjoinfilter-qualifier.md)
</dt> <dd>

Tipo de dados: **cadeia de caracteres**

Consulta WQL para filtrar instâncias depois que elas tiverem sido Unidas em uma classe de junção.

</dd> <dt>

<span id="PropertySources"></span><span id="propertysources"></span><span id="PROPERTYSOURCES"></span>[**PropertySources**](propertysources-qualifier.md)
</dt> <dd>

Tipo de dados: **matriz de cadeia de caracteres**

Propriedades de origem das quais uma propriedade de classe de exibição obtém dados.

</dd> <dt>

<span id="Union"></span><span id="union"></span><span id="UNION"></span>**Unida**
</dt> <dd>

Tipo de dados: **booliano**

Indica se você está definindo uma classe Union. As exibições de União contêm instâncias baseadas na União de instâncias de origem. Por exemplo, você pode declarar o seguinte:


```mof
Union, ViewSources{"SELECT Handle, Name, CreationDate FROM Win32_Process", 
                   "SELECT Caption, Name, ProcessHandle FROM Win32_Thread"}.
```



</dd> <dt>

<span id="ViewSources"></span><span id="viewsources"></span><span id="VIEWSOURCES"></span>[**ViewSources**](viewsources-qualifier.md)
</dt> <dd>

Tipo de dados: **matriz de cadeia de caracteres**

Conjunto de consultas de linguagem WQL (WQL) que definem as instâncias de origem e as propriedades usadas em uma classe de exibição específica. A correspondência posicional de todos os qualificadores de matriz é importante.

</dd> <dt>

<span id="ViewSpaces"></span><span id="viewspaces"></span><span id="VIEWSPACES"></span>[**ViewSpaces**](viewspaces-qualifier.md)
</dt> <dd>

Tipo de dados: **matriz de cadeia de caracteres**

Namespaces em que as instâncias de origem estão localizadas.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |



 

