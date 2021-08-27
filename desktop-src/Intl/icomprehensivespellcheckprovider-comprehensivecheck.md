---
description: Verifique o texto do provedor de maneira mais completa do que ISpellCheckProvider::Check.
ms.assetid: BD334EB8-4E14-478D-AB2A-E7F863C4BE0F
title: Método IComprehensiveSpellCheckProvider::ComprehensiveCheck
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
ms.openlocfilehash: ee1b07eb2f459aca3955b0a1c5ad2e2e2139cc196f618430b3039b1eba1e3971
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086596"
---
# <a name="icomprehensivespellcheckprovidercomprehensivecheck-method"></a>Método IComprehensiveSpellCheckProvider::ComprehensiveCheck

Verifique o texto do provedor de maneira mais completa do que [**ISpellCheckProvider::Check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ComprehensiveCheck(
  [in]  PCWSTR             text,
  [out] IEnumSpellingError **result
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*texto* \[ Em\]
</dt> <dd>

O texto a ser verificar.

</dd> <dt>

*resultado* \[ out\]
</dt> <dd>

O resultado da verificação desse texto, como uma enumeração de erros de ortografia ([**IEnumSpellingError),**](/windows/desktop/api/Spellcheck/nn-spellcheck-ienumspellingerror)se algum.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Valor retornado                                                                             | Descrição                           |
|------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>S \_ OK</dt> </dl>         | Bem sucedido.<br/>                |
| <dl> <dt>E \_ INVALIDARG</dt> </dl> | *text* é uma cadeia de caracteres vazia.<br/> |
| <dl> <dt>PONTEIRO \_ E</dt> </dl>    | *text* é um ponteiro nulo.<br/>  |



 

## <a name="remarks"></a>Comentários

Essa interface não é necessária para ser implementada por um provedor de verificação ort spell. Mas se o provedor dá suporte a dois "modos" de verificação ortícia (um mais rápido e um mais lento, mas mais completo), ele deve implementar essa interface no mesmo objeto que implementa [**ISpellCheckProvider**](/windows/desktop/api/Spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider) para dar suporte ao modo de verificação mais completo. Quando um cliente chama [**ISpellChecker::ComprehensiveCheck**](/windows/desktop/api/Spellcheck/nf-spellcheck-ispellchecker-comprehensivecheck), a funcionalidade de verificação ortotária [**consultará o**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) provedor para [**IComprehensiveSpellCheckProvider**](/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-icomprehensivespellcheckprovider)e chamará **IComprehensiveSpellCheckProvider.ComprehensiveCheck** se a interface tiver suporte. Se a interface não for suportada, ela retornará silenciosamente para [**ISpellCheckProvider::Check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check).

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

[**ISpellCheckProvider::Check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check)
</dt> </dl>

 

 
