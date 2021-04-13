---
description: O método Add do objeto SWbemQualifierSet adiciona um objeto SWbemQualifier à coleção SWbemQualifierSet. Se já existir um qualificador com o mesmo nome na coleção, ele será substituído.
ms.assetid: 8f4c4da2-4890-4515-a3dc-76d154dae43c
ms.tgt_platform: multiple
title: Método SWbemQualifierSet. Add (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet.Add
- ISWbemQualifierSet.Add
- ISWbemQualifierSet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: bbbef15ccc45aeba5b7e3c03f6cb9448cfe03ec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297489"
---
# <a name="swbemqualifiersetadd-method"></a>Método SWbemQualifierSet. Add

O método **Add** do objeto [**SWbemQualifierSet**](swbemqualifierset.md) adiciona um objeto [**SWbemQualifier**](swbemqualifier.md) à coleção **SWbemQualifierSet** . Se já existir um qualificador com o mesmo nome na coleção, ele será substituído.

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
objQualifier = .Add( _
  ByVal strName, _
  ByVal varVal, _
  [ ByVal bPropagatesToSubclasses ], _
  [ ByVal bPropagatesToInstances ], _
  [ ByVal bOverridable ], _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*strName* \[ no\]
</dt> <dd>

Obrigatórios. Nome do novo qualificador.

</dd> <dt>

*varVal* \[ no\]
</dt> <dd>

Obrigatórios. Valor da variante do novo qualificador.

</dd> <dt>

*bPropagatesToSubclasses* \[ em, opcional\]
</dt> <dd>

Valor booliano que indica se esse novo qualificador é propagado para subclasses. O valor padrão é **true**.

</dd> <dt>

*bPropagatesToInstances* \[ em, opcional\]
</dt> <dd>

Valor booliano que indica se esse novo qualificador é propagado para instâncias. O valor padrão é **true**.

</dd> <dt>

*bOverridable* \[ em, opcional\]
</dt> <dd>

Valor booliano que indica se este qualificador pode ser substituído quando propagado. O valor padrão é **true**.

</dd> <dt>

*iFlags* \[ em, opcional\]
</dt> <dd>

Reservado. O valor padrão é 0.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se for bem-sucedido, esse método retornará um objeto [**SWbemQualifier**](swbemqualifier.md) que representa o novo qualificador. Caso contrário, um objeto **nulo** será retornado.

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do método **Add** , o objeto **Err** pode conter um dos códigos de erro na lista a seguir.

<dl> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

O parâmetro *iFlags* não era válido.

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Erro não especificado.

</dd> <dt>

**wbemErrCannotBeKey** -2147749919 (0x8004101F)
</dt> <dd>

Houve uma tentativa inválida de especificar um qualificador de **chave** em uma propriedade que não pode ser uma chave. As chaves são especificadas na definição de classe para um objeto e não podem ser alteradas por instância.

</dd> <dt>

**wbemErrInvalidQualifierType** -2147749929 (0x80041029)
</dt> <dd>

O parâmetro *varVal* não é de um tipo de qualificador legal.

</dd> <dt>

**wbemErrOverrideNotAllowed** -2147749914 (0x8004101A)
</dt> <dd>

Não é possível executar a operação **SWbemQualifierSet. Add** neste qualificador porque o objeto proprietário não permite substituições.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMQUALIFIERSET CLSID<br/>                                                     |
| IID<br/>                      | ISWbemQualifierSet de IID \_<br/>                                                      |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemQualifierSet**](swbemqualifierset.md)
</dt> <dt>

[**SWbemQualifierSet. Remove**](swbemqualifierset-remove.md)
</dt> </dl>

 

 




