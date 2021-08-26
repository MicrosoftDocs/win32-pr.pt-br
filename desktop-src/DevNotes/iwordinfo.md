---
description: A interface IWordInfo é um componente de recurso de idioma específico do japonês. O objeto analisará o texto e identificará palavras individuais, retornando as palavras na cadeia de caracteres ou retornando as formas de dicionário (raiz) das palavras no texto da cadeia de caracteres.
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
ms.openlocfilehash: a82ff0c5d817dbec6d64d1d38d40245983877563416b30760926bb7522cd14c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001466"
---
# <a name="iwordinfo-interface"></a>Interface IWordInfo

\[Essa interface é obsoleta e não tem suporte no Windows Vista.\]

A interface **IWordInfo** é um componente de recurso de idioma específico do japonês. O objeto analisará o texto e identificará palavras individuais, retornando as palavras na cadeia de caracteres ou retornando as formas de dicionário (raiz) das palavras no texto da cadeia de caracteres.

## <a name="members"></a>Membros

A interface **IWordInfo** herda da interface [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IWordInfo** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IWordInfo** tem esses métodos.



| Método        | Descrição                                                                                                                                 |
|:--------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| **BreakText** | Analisar texto para identificar palavras e fornece os resultados para o [objeto WordSink.](/previous-versions//ms691570(v=vs.85))<br/> |



 

## <a name="remarks"></a>Comentários

Essa interface é usada para recuperar quebras de palavras em japonês ou formulários de dicionário para o texto a ser analisado. A forma de dicionário de uma palavra é a forma não desprotegida da palavra.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                   |
| Fim do suporte ao cliente<br/>    | Windows XP<br/>                                                                  |
| Fim do suporte ao servidor<br/>    | Windows Server 2003<br/>                                                         |
| DLL<br/>                      | <dl> <dt>Msir3jp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Wordinfo**](wordinfo-coclass.md)
</dt> <dt>

[WordSink](/previous-versions//ms691570(v=vs.85))
</dt> </dl>

 

 
