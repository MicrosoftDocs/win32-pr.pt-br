---
description: O método Add do objeto SWbemPrivilegeSet adiciona um objeto SWbemPrivilege à coleção SWbemPrivilegeSet. Se já existir um privilégio com o mesmo nome na coleção, ele será substituído.
ms.assetid: 7d44193f-60e1-4e83-8640-31d8df509d98
ms.tgt_platform: multiple
title: Método SWbemPrivilegeSet. Add (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.Add
- ISWbemPrivilegeSet.Add
- ISWbemPrivilegeSet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 080b9d3e3ab6dbfc0ed8afc8ac0476981b7c26e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010759"
---
# <a name="swbemprivilegesetadd-method"></a>Método SWbemPrivilegeSet. Add

O método **Add** do objeto [**SWbemPrivilegeSet**](swbemprivilegeset.md) adiciona um objeto [**SWbemPrivilege**](swbemprivilege.md) à coleção **SWbemPrivilegeSet** . Se já existir um privilégio com o mesmo nome na coleção, ele será substituído.

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
objPrivilege = .Add( _
  ByVal iPrivilege, _
  [ ByVal bIsEnabled ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*iPrivilege* 
</dt> <dd>

Obrigatórios. Uma das constantes do WMI do grupo [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) . Essas constantes são essencialmente inteiros que representam privilégios específicos. Por exemplo, para adicionar o privilégio que permite desligar um sistema de computador, use a constante **wbemPrivilegeShutdown** . Em um script, você deve usar o equivalente numérico de 23 (0x17). Para obter uma lista completa dessas constantes e as cadeias de caracteres de privilégio associadas, consulte [**constantes de privilégio**](privilege-constants.md).

</dd> <dt>

*bIsEnabled* \[ adicional\]
</dt> <dd>

Valor booliano que habilita ou desabilita esse privilégio. O valor padrão é **true**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se for bem-sucedido, o método retornará um objeto [**SWbemPrivilege**](swbemprivilege.md) que representa o novo privilégio. Caso contrário, um objeto nulo será retornado.

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do método **Add** , o objeto **Err** pode conter o código de erro na lista a seguir.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Erro não especificado.

</dd> </dl>

## <a name="examples"></a>Exemplos

Um exemplo de código usando esse método é descrito no tópico [**SWbemPrivilegeSet**](swbemprivilegeset.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMPRIVILEGESET CLSID<br/>                                                     |
| IID<br/>                      | ISWbemPrivilegeSet de IID \_<br/>                                                      |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemPrivilegeSet**](swbemprivilegeset.md)
</dt> <dt>

[Executando operações privilegiadas](executing-privileged-operations.md)
</dt> <dt>

[Executando operações privilegiadas usando o VBScript](executing-privileged-operations-using-vbscript.md)
</dt> <dt>

[**SWbemPrivilegeSet.AddAsString**](swbemprivilegeset-addasstring.md)
</dt> <dt>

[**SWbemPrivilegeSet. Remove**](swbemprivilegeset-remove.md)
</dt> <dt>

[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[**Constantes de privilégio**](privilege-constants.md)
</dt> </dl>

 

 




