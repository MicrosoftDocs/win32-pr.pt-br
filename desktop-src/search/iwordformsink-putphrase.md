---
description: Coloca uma forma alternativa de uma palavra no objeto IWordFormSink.
ms.assetid: 4F6A3E88-A17C-4CA3-849D-FF0DC06D5DC3
title: Método IWordFormSink::P utAltWord (Search.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordFormSink.PutAltWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 874428ed435d2336398f6e72c58b70de275565cce2e606f1fdddea54f0684742
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944406"
---
# <a name="iwordformsinkputaltword-method"></a>Método IWordFormSink::P utAltWord

Coloca uma forma alternativa de uma palavra no [**objeto IWordFormSink.**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT PutAltWord(
  [in] const WCHAR *pwcInBuf ,
  [in]       ULONG cwc
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pwcInBuf* \[ Em\]
</dt> <dd>

Um ponteiro para um buffer que contém uma forma alternativa de uma palavra.

</dd> <dt>

*cwc* \[ Em\]
</dt> <dd>

O número de caracteres *em pwcInBuf*.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                                              | Descrição                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                     | A operação foi concluída com êxito. <br/>                                                                                             |
| <dl> <dt>**LANGUAGE \_ S \_ LARGE \_ WORD**</dt> </dl> | O valor *de cwc* é maior que o valor de *ulMaxTokenSize* especificado em [**IStemmer::Init**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-init). <br/> |



 

## <a name="remarks"></a>Comentários

Esse método é chamado do método [**GenerateWordForms**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-generatewordforms) da implementação [**do IStemmer.**](/windows/win32/api/indexsrv/nn-indexsrv-istemmer) Todos os formulários alternativos para uma palavra, exceto o último, são colocados no objeto [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) chamando **IWordFormSink::P utAltWord**. A forma alternativa final de uma palavra, que é sempre a forma original da palavra, é tratada chamando [**IWordFormSink::P utWord**](iwordformsink-putword.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Search.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink)
</dt> </dl>

 

 
