---
description: 'Verifique a ortografia do texto do provedor de maneira mais completa do que ISpellCheckProvider:: check.'
ms.assetid: BD334EB8-4E14-478D-AB2A-E7F863C4BE0F
title: 'Método IComprehensiveSpellCheckProvider:: ComprehensiveCheck'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IComprehensiveSpellCheckProvider.ComprehensiveCheck
api_type:
- COM
api_location:
- spellcheckprovider.h
ms.openlocfilehash: d999a90166e0d54d537abc84c30f6c4e0ee3768c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782926"
---
# <a name="icomprehensivespellcheckprovidercomprehensivecheck-method"></a>Método IComprehensiveSpellCheckProvider:: ComprehensiveCheck

Verifique a ortografia do texto do provedor de maneira mais completa do que [**ISpellCheckProvider:: check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ComprehensiveCheck(
  [in]  PCWSTR             text,
  [out] IEnumSpellingError **result
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*texto* \[ de no\]
</dt> <dd>

O texto a ser verificado.

</dd> <dt>

*resultado* \[ fora\]
</dt> <dd>

O resultado da verificação desse texto, como uma enumeração de erros de ortografia ([**IEnumSpellingError**](/windows/desktop/api/Spellcheck/nn-spellcheck-ienumspellingerror)), se houver.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Valor retornado                                                                             | Descrição                           |
|------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>S \_ OK</dt> </dl>         | Bem-sucedida.<br/>                |
| <dl> <dt>E \_ INVALIDARG</dt> </dl> | o *texto* é uma cadeia de caracteres vazia.<br/> |
| <dl> <dt>\_ponteiro E</dt> </dl>    | o *texto* é um ponteiro nulo.<br/>  |



 

## <a name="remarks"></a>Comentários

Essa interface não precisa ser implementada por um provedor de verificação ortográfica. Mas se o provedor oferecer suporte a dois "modos" de verificação ortográfica (uma mais rápida e mais lenta, mas mais completa), ele deverá implementar essa interface no mesmo objeto que implementa o [**ISpellCheckProvider**](/windows/desktop/api/Spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider) para dar suporte ao modo de verificação mais completo. Quando um cliente chama [**ISpellChecker:: ComprehensiveCheck**](/windows/desktop/api/Spellcheck/nf-spellcheck-ispellchecker-comprehensivecheck), a funcionalidade de verificação ortográfica fará a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) do provedor para [**IComprehensiveSpellCheckProvider**](/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-icomprehensivespellcheckprovider)e chamará **IComprehensiveSpellCheckProvider. ComprehensiveCheck** se a interface tiver suporte. Se a interface não tiver suporte, ela será revertida silenciosamente para [**ISpellCheckProvider:: check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check).

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IComprehensiveSpellCheckProvider**](/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-icomprehensivespellcheckprovider)
</dt> <dt>

[**IEnumSpellingError**](/windows/desktop/api/Spellcheck/nn-spellcheck-ienumspellingerror)
</dt> <dt>

[**ISpellChecker::ComprehensiveCheck**](/windows/desktop/api/Spellcheck/nf-spellcheck-ispellchecker-comprehensivecheck)
</dt> <dt>

[**ISpellCheckProvider**](/windows/desktop/api/Spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider)
</dt> <dt>

[**ISpellCheckProvider:: verificar**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check)
</dt> </dl>

 

 
