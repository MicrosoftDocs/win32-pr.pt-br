---
description: O método Add do objeto SWbemPropertySet adiciona um objeto SWbemProperty à coleção SWbemPropertySet. Se já existir uma propriedade com o mesmo nome na coleção, seu conteúdo será substituído pela nova definição.
ms.assetid: 52a5f964-3d53-441b-9a58-650afdc5b1b9
ms.tgt_platform: multiple
title: Método SWbemPropertySet. Add (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet.Add
- ISWbemPropertySet.Add
- ISWbemPropertySet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1ad5b40d31d162b287bdb1a387cd0602e0be1ce6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105814421"
---
# <a name="swbempropertysetadd-method"></a>Método SWbemPropertySet. Add

O método **Add** do objeto [**SWbemPropertySet**](swbempropertyset.md) adiciona um objeto [**SWbemProperty**](swbemproperty.md) à coleção **SWbemPropertySet** . Se já existir uma propriedade com o mesmo nome na coleção, seu conteúdo será substituído pela nova definição.

> [!Note]  
> O valor da propriedade adicionada é **nulo** (não atribuído) após esta operação. Para definir ou alterar o valor de uma propriedade WMI, você deve definir a propriedade [**Value**](swbemdatetime-value.md) do objeto [**SWbemProperty**](swbemproperty.md) retornado.

 

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
objProperty = .Add( _
  ByVal strName, _
  ByVal iCIMType, _
  [ ByVal bIsArray ], _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*strName* \[ no\]
</dt> <dd>

Obrigatórios. Nome da nova propriedade.

</dd> <dt>

*iCIMType* \[ no\]
</dt> <dd>

Obrigatórios. Um inteiro que representa o qualificador **CIMType** da nova propriedade. Consulte [**WbemCimTypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum) para obter a lista com os qualificadores **CIMType** e seus valores.

</dd> <dt>

*bIsArray* \[ em, opcional\]
</dt> <dd>

Especifica se a propriedade é um tipo de matriz. O valor padrão para esse parâmetro é **false**.

</dd> <dt>

*iFlags* \[ em, opcional\]
</dt> <dd>

Reservado e deve ser zero se especificado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se for bem-sucedido, esse método retornará um objeto [**SWbemProperty**](swbemproperty.md) que representa a nova propriedade. Caso contrário, um objeto **nulo** será retornado.

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do método **Add** , o objeto **Err** pode conter um dos códigos de erro abaixo.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Falha não especificada.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Foi especificado um parâmetro inválido.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Não há memória suficiente para execução deste método.

</dd> <dt>

**wbemErrInvalidPropertyType** -2147749930
</dt> <dd>

O qualificador **CIMType** não é reconhecido.

</dd> </dl>

## <a name="examples"></a>Exemplos

Para obter um exemplo de código que usa esse método, consulte o tópico [**SWbemPropertySet**](swbempropertyset.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMPROPERTYSET CLSID<br/>                                                      |
| IID<br/>                      | ISWbemPropertySet de IID \_<br/>                                                       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemPropertySet**](swbempropertyset.md)
</dt> <dt>

[**SWbemPropertySet. Remove**](swbempropertyset-remove.md)
</dt> <dt>

[**SWbemProperty. Value**](swbemproperty-value.md)
</dt> </dl>

 

 




