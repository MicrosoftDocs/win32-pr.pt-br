---
description: Atualiza os dados para objetos que têm dados fornecidos por um provedor de desempenho, como as classes de contador de desempenho. Você pode obter dados atualizados mais rapidamente e sem uma chamada para SWbemServices. get \_ .
ms.assetid: 6aeaa336-fb98-4eda-b746-fc958198d8ae
ms.tgt_platform: multiple
title: Método de SWbemObjectEx.Refresh_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx.Refresh_
- ISWbemObjectEx.Refresh_
- ISWbemObjectEx.Refresh_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 904e2b7f9b256596555c8396a699220108d4f37b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771304"
---
# <a name="swbemobjectexrefresh_-method"></a>Método SWbemObjectEx. Refresh \_

O **método \_ Refresh** de [**SWbemObjectEx**](swbemobjectex.md) atualiza os dados de objetos que têm dados fornecidos por um provedor de desempenho, como as [classes de contador de desempenho](/windows/desktop/CIMWin32Prov/performance-counter-classes). Você pode obter dados atualizados mais rapidamente e sem uma chamada para [**SWbemServices. get \_**](swbemservices-get.md).

Para obter mais informações sobre essa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
SWbemObjectEx.Refresh_( _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*iFlags* \[ em, opcional\]
</dt> <dd>

Sinalizadores de operação reservados que, se especificados, devem ser 0 (zero).

</dd> <dt>

*objWbemNamedValueSet* \[ em, opcional\]
</dt> <dd>

Um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que define o contexto para a operação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do **método \_ Refresh** , o objeto **Err** pode conter um dos códigos de erro na lista a seguir.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

O provedor falhou internamente, embora a operação fosse válida.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002)
</dt> <dd>

O formato solicitado não foi encontrado.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Um dos parâmetros para a chamada não está correto.

</dd> <dt>

**wbemErrRefresherBusy** -2147749975 (0x80041057)
</dt> <dd>

O atualizador está ocupado com outra operação.

</dd> <dt>

**wbemPartialResults** -2147745808 (0x80040010)
</dt> <dd>

Nem todos os objetos, enumeradores ou atualizadores aninhados foram atualizados com êxito. Esse retorno não é um erro, mas uma indicação de que a operação estava incompleta.

</dd> </dl>

## <a name="examples"></a>Exemplos

O exemplo de código de script a seguir mostra como obter contadores de desempenho brutos e cooked para o processo do sistema. Os objetos são atualizados a cada dois segundos e as propriedades são exibidas.


```VB
' Get the performance counter instance for the System process
set PerfRaw = GetObject( _
    "winmgmts:win32_perfrawdata_perfproc_process.name='system'")
set PerfCooked = GetObject( _
    "winmgmts:win32_perfformatteddata_perfproc_process.name='system'")

' Display some properties in a loop
for I = 1 to 5
    Wscript.Echo "HandleCount = "& PerfRaw.HandleCount & _
         " Raw ThreadCount = " & PerfRaw.ThreadCount & _
        " Cooked ThreadCount = " & PerfCooked.ThreadCount
    
    Wscript.Sleep 2000
    
' Refresh the objects
    PerfRaw.Refresh_
    PerfCooked.Refresh_
next
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMOBJECTEX CLSID<br/>                                                         |
| IID<br/>                      | ISWbemObjectEx de IID \_<br/>                                                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemObjectEx**](swbemobjectex.md)
</dt> <dt>

[Monitorando dados de desempenho](monitoring-performance-data.md)
</dt> </dl>

 

