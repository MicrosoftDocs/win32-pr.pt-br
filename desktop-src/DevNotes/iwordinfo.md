---
description: A interface IWordInfo é um componente de recurso de linguagem específico do japonês. O objeto analisa o texto e identifica palavras individuais, retornando as palavras na cadeia de caracteres ou retorna os formulários de dicionário (raiz) das palavras no texto da cadeia de caracteres.
ms.assetid: 760d9c78-d564-40a2-b2e4-d538c32361ed
title: Interface IWordInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordInfo
- IWordInfo.BreakText
api_type:
- COM
api_location:
- Msir3jp.dll
ms.openlocfilehash: 9d685f2aa1b4ba4d31f221812c12729e4e689360
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500781"
---
# <a name="iwordinfo-interface"></a>Interface IWordInfo

\[Essa interface é obsoleta e não tem suporte no Windows Vista.\]

A interface **IWordInfo** é um componente de recurso de linguagem específico do japonês. O objeto analisa o texto e identifica palavras individuais, retornando as palavras na cadeia de caracteres ou retorna os formulários de dicionário (raiz) das palavras no texto da cadeia de caracteres.

## <a name="members"></a>Membros

A interface **IWordInfo** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IWordInfo** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IWordInfo** tem esses métodos.



| Método        | Descrição                                                                                                                                 |
|:--------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| **BreakText** | Analisa o texto para identificar palavras e fornece os resultados para o objeto [WordSink](/previous-versions//ms691570(v=vs.85)) .<br/> |



 

## <a name="remarks"></a>Comentários

Essa interface é usada para recuperar as quebras de palavra japonesas ou os formulários de dicionário para o texto a ser analisado. A forma de dicionário de uma palavra é a forma uninflected da palavra.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                   |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                                                  |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                         |
| DLL<br/>                      | <dl> <dt>Msir3jp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**WordInfo**](wordinfo-coclass.md)
</dt> <dt>

[WordSink](/previous-versions//ms691570(v=vs.85))
</dt> </dl>

 

 
