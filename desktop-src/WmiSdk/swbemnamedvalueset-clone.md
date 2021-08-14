---
description: O método Clone do objeto SWbemNamedValueSet retorna um novo objeto que é um clone da coleção atual.
ms.assetid: 0e7fab2e-8175-45e5-aa70-1109502e2b3f
ms.tgt_platform: multiple
title: Método SWbemNamedValueSet.Clone (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Clone
- ISWbemNamedValueSet.Clone
- ISWbemNamedValueSet.Clone
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9158901a39fa80e49404912ee5458c416069bbe354e19059ef4622ae4257fda9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118314187"
---
# <a name="swbemnamedvaluesetclone-method"></a>Método SWbemNamedValueSet.Clone

O **método Clone** do objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) retorna um novo objeto que é um clone da coleção atual.

Para uma explicação dessa sintaxe, consulte [Convenções de documento para a API de Script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
objwbemNamedValueSet = .Clone( _
)
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Se for bem-sucedido, [**um novo objeto SWbemNamedValueSet**](swbemnamedvalueset.md) retornará.

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do **método Clone,** o **objeto Err** pode conter um dos códigos de erro abaixo.

<dl> <dt>

**wbemErrFailed** – 2147749889 (0x80041001)
</dt> <dd>

Erro não especificado.

</dd> <dt>

**wbemErrOutOfMemory** – 2147749894 (0x80041006)
</dt> <dd>

Não há memória suficiente para clonar o objeto.

</dd> </dl>

## <a name="remarks"></a>Comentários

Use esse método para duplicar uma [**coleção SWbemNamedValueSet.**](swbemnamedvalueset.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemNamedValueSet<br/>                                                    |
| IID<br/>                      | IID \_ ISWbemNamedValueSet<br/>                                                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemNamedValueSet**](swbemnamedvalueset.md)
</dt> </dl>

 

 




