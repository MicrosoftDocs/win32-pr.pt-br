---
description: O método Cancel do objeto SWbemSink cancela todas as operações assíncronas pendentes associadas a esse coletor de objeto.
ms.assetid: dbe1eb24-5d9d-407a-b7c6-c58ec6891d7a
ms.tgt_platform: multiple
title: 'Método ISWbemSink:: Cancel (Wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.Cancel
- ISWbemSink.Cancel
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 37bb44e8c34aa3cd7f9d491656461097e5a2bb5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171969"
---
# <a name="iswbemsinkcancel-method"></a>Método ISWbemSink:: Cancel

O método **Cancel** do objeto [**SWbemSink**](swbemsink.md) cancela todas as operações assíncronas pendentes associadas a esse coletor de objeto.

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
SWbemSink.Cancel()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do método **Cancel** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter um dos códigos de erro abaixo.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Erro não especificado.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Não há memória suficiente para concluir a operação.

</dd> <dt>

**wbemErrTransportFailure** -2147749909 (0x80041015)
</dt> <dd>

Ocorreu um erro de rede, impedindo a operação normal.

</dd> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

O nome de usuário e a senha atuais ou especificados não são válidos ou autorizados a estabelecer a conexão.

</dd> </dl>

## <a name="remarks"></a>Comentários

Não é possível cancelar apenas uma chamada assíncrona. Se várias chamadas assíncronas estiverem pendentes que usam esse coletor de objeto, esse método cancelará todas as chamadas assíncronas usando esse coletor de objeto. As chamadas assíncronas associadas a outros coletores de objetos continuam inalteradas.

Não é possível atribuir esse coletor a **nada** para cancelar uma operação assíncrona. Você deve chamar o método **Cancel** para tornar o WMI descontinuar a operação e liberar os recursos associados. Isso é muito importante com operações assíncronas demoradas, como consultas ou operações que nunca são concluídas, como [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md).

> [!Note]  
> Um retorno de chamada assíncrono permite que um usuário não autenticado forneça dados para o coletor. Isso representa riscos de segurança para seus scripts e aplicativos. Para eliminar os riscos, use semisynchronous ou comunicação síncrona. Para obter mais informações, consulte [chamando um método](calling-a-method.md).

 

O exemplo a seguir mostra como cancelar uma chamada assíncrona.


```VB
objwbemsink.Cancel()
set objwbemsink= Nothing
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Wbemdisp. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMSINK CLSID<br/>                                                             |
| IID<br/>                      | ISWbemSink de IID \_<br/>                                                              |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemSink**](swbemsink.md)
</dt> </dl>

 

