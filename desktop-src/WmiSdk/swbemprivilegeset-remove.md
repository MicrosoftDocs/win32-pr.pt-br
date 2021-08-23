---
description: O método Remove do objeto SWbemPrivilegeSet exclui um privilégio da coleção.
ms.assetid: 4c0b6d49-262c-4840-955b-35b16b68f29f
ms.tgt_platform: multiple
title: Método SWbemPrivilegeSet.Remove (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.Remove
- ISWbemPrivilegeSet.Remove
- ISWbemPrivilegeSet.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 825fbdc18537fa73561f8a662ecc0388ab18be0b9bf26ca2cbfeadd7bfb9b469
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119732286"
---
# <a name="swbemprivilegesetremove-method"></a>Método SWbemPrivilegeSet.Remove

O **método** Remove do objeto [**SWbemPrivilegeSet**](swbemprivilegeset.md) exclui um privilégio da coleção.

Para uma explicação dessa sintaxe, consulte [Convenções de documento para a API de Script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
SWbemPrivilegeSet.Remove( _
  ByVal iPrivilege _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*iPrivilege* 
</dt> <dd>

Obrigatórios. Essa é uma das constantes WMI do [**grupo WbemPrivilegeEnum.**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) Essas constantes são essencialmente inteiros que representam privilégios específicos. Por exemplo, para remover o privilégio que permite desligar um sistema Windows, use a constante **wbemPrivilegeShutdown** ou o equivalente numérico de 0x17.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do **método Remove,** o **objeto Err** pode conter um dos códigos de erro na lista a seguir.

<dl> <dt>

**wbemErrFailed** – 2147749889 (0x80041001)
</dt> <dd>

Erro não especificado.

</dd> <dt>

**wbemErrNotFound** – 2147749890 (0x80041002)
</dt> <dd>

O privilégio especificado não existe.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemPrivilegeSet<br/>                                                     |
| IID<br/>                      | IID \_ ISWbemPrivilegeSet<br/>                                                      |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemPrivilegeSet**](swbemprivilegeset.md)
</dt> <dt>

[**SWbemPrivilegeSet.Add**](swbemprivilegeset-add.md)
</dt> </dl>

 

 




