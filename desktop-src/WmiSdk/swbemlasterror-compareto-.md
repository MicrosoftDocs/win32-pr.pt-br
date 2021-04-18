---
description: O \_ método CompareTo do objeto SWbemLastError compara dois objetos SWbemObject. Essa comparação está sujeita a determinadas restrições com base nos valores especificados no parâmetro iFlags.
ms.assetid: 541510e4-ef8d-4436-966f-19c5df422281
ms.tgt_platform: multiple
title: Método de SWbemLastError.CompareTo_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.CompareTo_
- ISWbemLastError.CompareTo_
- ISWbemLastError.CompareTo_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4c24eb6e57e81c6c44922b2d6643be65198951ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771277"
---
# <a name="swbemlasterrorcompareto_-method"></a>Método SWbemLastError. CompareTo \_

O **método \_ CompareTo** do objeto [**SWbemLastError**](swbemlasterror.md) compara dois objetos [**SWbemObject**](swbemobject.md) . Essa comparação está sujeita a determinadas restrições com base nos valores especificados no parâmetro *iFlags* .

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
bAreEqual = .CompareTo_( _
  ByVal objwbemObject, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*objwbemObject* \[ no\]
</dt> <dd>

Obrigatórios. Um objeto de classe [**SWbemObject**](swbemobject.md) . Esse parâmetro é o objeto com o qual o primeiro objeto é comparado. O objeto deve ser uma instância de **SWbemObject** válida.

</dd> <dt>

*iFlags* \[ em, opcional\]
</dt> <dd>

Um inteiro que especifica sinalizadores adicionais para a operação. Esse parâmetro especifica as características do objeto a serem consideradas quando comparações de objeto são feitas. Você pode usar **wbemComparisonFlagIncludeAll** para considerar todos os recursos (padrão) ou qualquer combinação dos valores a seguir.

<dt>

<span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>

<span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>wbemComparisonFlagIncludeAll * * * * (0 (0x0))


</dt> <dd>

Faz com que todas as propriedades, qualificadores e tipos sejam comparados.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>

<span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>wbemComparisonFlagIgnoreQualifiers * * * * (1 (0x1))


</dt> <dd>

Faz com que todos os qualificadores (incluindo a **chave** e **dinâmica**) sejam ignorados em comparação.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>

<span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>wbemComparisonFlagIgnoreObjectSource * * * * (2 (0x2))


</dt> <dd>

Faz com que a origem dos objetos, ou seja, o servidor e o namespace do qual eles vieram, sejam ignorados em comparação com outros objetos.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>

<span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>wbemComparisonFlagIgnoreDefaultValues * * * * (4 (0x4))


</dt> <dd>

Faz com que os valores padrão das propriedades sejam ignorados. Esse sinalizador só é significativo para comparar classes.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>

<span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>wbemComparisonFlagIgnoreClass * * * * (8 (0x8))


</dt> <dd>

Instrui o sistema a assumir que os objetos sendo comparados são instâncias da mesma classe. Consequentemente, esse sinalizador compara apenas informações relacionadas à instância. Use este sinalizador para otimizar o desempenho. Se os objetos não são da mesma classe, os resultados são indefinidos.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>

<span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>wbemComparisonFlagIgnoreCase * * * * (16 (0x10))


</dt> <dd>

Faz com que os valores de cadeia de caracteres sejam comparados de maneira não diferencia maiúsculas de minúsculas. Isso se aplica tanto a cadeias de caracteres quanto a valores de qualificador. Nomes de propriedade e de qualificador sempre são comparados sem diferenciação de maiúsculas e minúsculas, seja este sinalizador especificado ou não.

</dd> <dt>

<span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>

<span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>wbemComparisonFlagIgnoreFlavor * * * * (32 (0x20))


</dt> <dd>

Faz com que os tipos de qualificador sejam ignorados. Este sinalizador ainda considera valores de qualificador, mas ignora diferenças de tipo como regras de propagação e restrições de substituição.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Retornar valor

O **método \_ CompareTo** retornará o valor booliano **true** se os objetos corresponderem; caso contrário, retornará **false**.

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do método **CompareTo \_** , o objeto **Err** pode conter um dos códigos de erro na lista a seguir.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Erro não especificado.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Um parâmetro especificado não é válido.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Não há memória suficiente para concluir a operação.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMLASTERROR CLSID<br/>                                                        |
| IID<br/>                      | ISWbemLastError de IID \_<br/>                                                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemLastError**](swbemlasterror.md)
</dt> <dt>

[**SWbemObject**](swbemobject.md)
</dt> </dl>

 

 




