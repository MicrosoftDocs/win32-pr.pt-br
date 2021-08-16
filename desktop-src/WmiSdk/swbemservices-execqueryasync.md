---
description: SWbemServices.Exemétodo cQueryAsync – executa uma consulta para recuperar objetos.
ms.assetid: 50c7f62b-dd83-4117-b10e-acee1690ce8c
ms.tgt_platform: multiple
title: SWbemServices.Exemétodo cQueryAsync (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecQueryAsync
- ISWbemServices.ExecQueryAsync
- ISWbemServices.ExecQueryAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 93b80f7571630b306951c9efddef459930b23ab66a0f1b62913836f459db8033
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312645"
---
# <a name="swbemservicesexecqueryasync-method"></a>SWbemServices.Exemétodo cQueryAsync

O **método ExecQueryAsync** do [**objeto SWbemServices**](swbemservices.md) executa uma consulta para recuperar objetos. A chamada para esse método retorna imediatamente e os resultados e o status são retornados ao chamador por meio de eventos entregues ao sink especificado em *objWbemSink.* Para manipular cada objeto retornado, crie *um objWbemSink.* Sub-rotina de evento [**OnObjectReady.**](swbemsink-onobjectready.md)

O método é chamado no modo assíncrono. Para obter mais informações, consulte [Chamando um método](calling-a-method.md).

Para uma explicação dessa sintaxe, consulte [Convenções de documento para a API de Script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
objWbemObjectSet = .ExecQueryAsync( _
  [ ByVal objWbemSink ], _
  ByVal strQuery, _
  [ ByVal strQueryLanguage ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*objWbemSink* \[ Opcional\]
</dt> <dd>

O sink do objeto que executa a consulta de forma assíncrona. Crie um [**objeto SWbemSink**](swbemsink.md) para receber os objetos.

</dd> <dt>

*strQuery* 
</dt> <dd>

Obrigatórios. Cadeia de caracteres que contém o texto da consulta. Esse parâmetro não pode estar em branco. Para obter mais informações sobre como criar cadeias de caracteres de consulta WMI, consulte Consultando com [WQL](querying-with-wql.md) e a [referência WQL.](wql-sql-for-wmi.md)

</dd> <dt>

*strQueryLanguage* \[ Opcional\]
</dt> <dd>

Cadeia de caracteres que contém a linguagem de consulta a ser usada. Se especificado, o valor deverá ser "WQL".

</dd> <dt>

*iFlags* \[ Opcional\]
</dt> <dd>

Inteiro que determina o comportamento da consulta. Esse parâmetro pode aceitar os valores a seguir.

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus*** (128 (0x80))


</dt> <dd>

Faz com que chamadas assíncronas enviem atualizações de status para o manipulador de eventos [**OnProgress**](swbemsink-onprogress.md) para o sink do objeto.

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus*** (0 (0x0))


</dt> <dd>

Impede que chamadas assíncronas enviem atualizações de status para o manipulador de eventos [**OnProgress**](swbemsink-onprogress.md) para o sink do objeto.

</dd> <dt>

<span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>

<span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>wbemQueryFlagPrototype*** (2 (0x2))


</dt> <dd>

Usado para um protótipo. Ele impede que a consulta ocorra e, em vez disso, retorna um objeto que se parece com um objeto de resultado típico.

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers*** (131072 (0x20000))


</dt> <dd>

Faz com que o WMI retorne dados de alteração de classe com a definição de classe base. Para obter mais informações, consulte [Localizando informações de classe WMI](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[ Opcional\]
</dt> <dd>

Normalmente, isso é indefinido. Caso contrário, esse é [**um objeto SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que serviços a solicitação. Um provedor que dá suporte ou requer informações de contexto deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.

</dd> <dt>

*objWbemAsyncContext* \[ Opcional\]
</dt> <dd>

Um [**objeto SWbemNamedValueSet**](swbemnamedvalueset.md) que retorna ao sink do objeto para identificar a origem da chamada assíncrona original. Use esse parâmetro para fazer várias chamadas assíncronas usando o mesmo sink de objeto. Para usar esse parâmetro, crie um objeto **SWbemNamedValueSet** e use o método [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) para adicionar um valor que identifica a chamada assíncrona que você está fazendo. Esse **objeto SWbemNamedValueSet** é retornado ao sink do objeto e a origem da chamada pode ser extraída usando o [**método SWbemNamedValueSet.Item.**](swbemnamedvalueset-item.md) Para obter mais informações, consulte [Chamando um método](calling-a-method.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não tem valores de retorno. Se for bem-sucedido, o sink receberá um [**evento OnObjectReady**](swbemsink-onobjectready.md) por instância. Após a última instância, o sink do objeto recebe [**um evento OnCompleted.**](swbemsink-oncompleted.md)

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do **método ExecQueryAsync,** o [objeto Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter um dos códigos de erro na lista a seguir.

<dl> <dt>

**wbemErrAccessDenied** – 2147749891 (0x80041003)
</dt> <dd>

O usuário atual não tem a permissão para exibir o conjunto de resultados.

</dd> <dt>

**wbemErrFailed** – 2147749889 (0x80041001)
</dt> <dd>

Erro não especificado.

</dd> <dt>

**wbemErrInvalidParameter** – 2147749896 (0x80041008)
</dt> <dd>

Parâmetro inválido foi especificado.

</dd> <dt>

**wbemErrInvalidQuery** – 2147749911 (0x80041017)
</dt> <dd>

A sintaxe de consulta não é válida.

</dd> <dt>

**wbemErrInvalidQueryType** – 2147749912 (0x80041018)
</dt> <dd>

Não há suporte para a linguagem de consulta solicitada.

</dd> <dt>

**wbemErrOutOfMemory** – 2147749894 (0x80041006)
</dt> <dd>

Não há memória suficiente para concluir a operação.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa chamada retorna imediatamente. Os objetos e o status solicitados são retornados ao chamador por meio de retornos de chamada entregues ao sink especificado em *objWbemSink.* Para processar cada objeto quando ele retornar, crie *um objWbemSink.* Sub-rotina de evento [**OnObjectReady.**](swbemsink-onobjectready.md) Depois que todos os objetos são retornados, execute o processamento final em sua implementação do *objWbemSink.* [**Evento OnCompleted.**](swbemsink-oncompleted.md)

Um retorno de chamada assíncrono permite que um usuário não autenticado forneça dados para o sink. Isso representa riscos de segurança para seus scripts e aplicativos. Para eliminar os riscos, consulte [Configurando a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md)

O **método ExecQueryAsync** retorna um conjunto de resultados vazio quando não há objetos para corresponder aos critérios na consulta. Esse método retorna as propriedades de chave, independentemente de a propriedade [**Key**](standard-qualifiers.md) ser solicitada ou não no *parâmetro strQuery.*

Há limites para o número de palavras-chave **AND** e **OR** que podem ser usadas em consultas WQL. Um grande número de palavras-chave WQL usadas em uma consulta complexa pode fazer com que o WMI retorne o código de erro WBEM E QUOTA VIOLATION como \_ \_ um valor \_ **HRESULT.** O limite de palavras-chave WQL depende de quão complexa a consulta é.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemServices<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemServices<br/>                                                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemServices**](swbemservices.md)
</dt> <dt>

[Chamando um método](calling-a-method.md)
</dt> <dt>

[**SWbemServices.Get**](swbemservices-get.md)
</dt> </dl>

 

