---
description: O método Add do objeto SWbemQualifierSet adiciona um objeto SWbemQualifier à coleção SWbemQualifierSet. Se um qualificador com o mesmo nome já existir na coleção, ele será substituído.
ms.assetid: 8f4c4da2-4890-4515-a3dc-76d154dae43c
ms.tgt_platform: multiple
title: Método SWbemQualifierSet.Add (Wbemdisp.h)
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
ms.openlocfilehash: 64a85e10614595d9dd6492d3f4b412f1d89432c0188801ea60a09e294846297b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897776"
---
# <a name="swbemqualifiersetadd-method"></a>Método SWbemQualifierSet.Add

O **método Add** do objeto [**SWbemQualifierSet**](swbemqualifierset.md) adiciona um objeto [**SWbemQualifier**](swbemqualifier.md) à **coleção SWbemQualifierSet.** Se um qualificador com o mesmo nome já existir na coleção, ele será substituído.

Para uma explicação dessa sintaxe, consulte [Convenções de documento para a API de Script](document-conventions-for-the-scripting-api.md).

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

*strName* \[ Em\]
</dt> <dd>

Obrigatórios. Nome do novo qualificador.

</dd> <dt>

*varVal* \[ Em\]
</dt> <dd>

Obrigatórios. Valor variante do novo qualificador.

</dd> <dt>

*bPropagatesToSubclasses* \[ in, opcional\]
</dt> <dd>

Valor booliana que indica se esse novo qualificador é propagado para subclasses. O valor padrão é **TRUE.**

</dd> <dt>

*bPropagatesToInstances* \[ in, opcional\]
</dt> <dd>

Valor booliana que indica se esse novo qualificador é propagado para instâncias. O valor padrão é **TRUE.**

</dd> <dt>

*bOverridable* \[ in, opcional\]
</dt> <dd>

Valor booliana que indica se esse qualificador pode ser substituído quando propagado. O valor padrão é **TRUE.**

</dd> <dt>

*iFlags* \[ in, opcional\]
</dt> <dd>

Reservado. O valor padrão é 0.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se for bem-sucedido, esse método retornará [**um objeto SWbemQualifier**](swbemqualifier.md) que representa o novo qualificador. Caso contrário, **um objeto nulo** será retornado.

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do **método Add,** o **objeto Err** pode conter um dos códigos de erro na lista a seguir.

<dl> <dt>

**wbemErrInvalidParameter** – 2147749896 (0x80041008)
</dt> <dd>

O *parâmetro iFlags* não era válido.

</dd> <dt>

**wbemErrFailed** – 2147749889 (0x80041001)
</dt> <dd>

Erro não especificado.

</dd> <dt>

**wbemErrCannotBeKey** – 2147749919 (0x8004101F)
</dt> <dd>

Houve uma tentativa ilegal de especificar um **qualificador** de chave em uma propriedade que não pode ser uma chave. As chaves são especificadas na definição de classe para um objeto e não podem ser alteradas por instância.

</dd> <dt>

**wbemErrInvalidQualifierType** – 2147749929 (0x80041029)
</dt> <dd>

O *parâmetro varVal* não é de um tipo qualificador legal.

</dd> <dt>

**wbemErrOverrideNotAllowed** – 2147749914 (0x8004101A)
</dt> <dd>

Não é possível executar a **operação SWbemQualifierSet.Add** nesse qualificador porque o objeto de propriedade não permite substituições.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemQualifierSet<br/>                                                     |
| IID<br/>                      | IID \_ ISWbemQualifierSet<br/>                                                      |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemQualifierSet**](swbemqualifierset.md)
</dt> <dt>

[**SWbemQualifierSet.Remove**](swbemqualifierset-remove.md)
</dt> </dl>

 

 




