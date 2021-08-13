---
title: WM/Codificaçãotime
description: O atributo WM/Encodingtime contém um carimbo de data/hora da hora em que o conteúdo foi codificado.
ms.assetid: 63da9392-264d-40bb-99fd-56db93801941
keywords:
- Formato de mídia do WM/Encodingtime Windows
topic_type:
- apiref
api_name:
- WM/EncodingTime
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20c76de789bd6ca88a9bbc2f3bb68381b3816524a07cbf97dc1a35b2526179a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118431820"
---
# <a name="wmencodingtime"></a>WM/Codificaçãotime

O atributo **WM/encodingtime** contém um carimbo de data/hora da hora em que o conteúdo foi codificado.

## <a name="global-constant"></a>Constante global

g \_ wszWMEncodingTime

## <a name="data-type"></a>Tipo de Dados

**FILETIME** (**WMT \_ tipo \_ QWORD**)

## <a name="remarks"></a>Comentários

Esse atributo usa um valor FILETIME, que é um valor de 64 bits que representa o número de unidades de tempo de 100 nanossegundos decorridos desde 1º de janeiro de 1601. para obter mais informações sobre o FILETIME, consulte a seção Windows Informações do Sistema do SDK da plataforma.

Este não é um atributo codificado. Você deve defini-lo manualmente se quiser incluí-lo em seus arquivos.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




