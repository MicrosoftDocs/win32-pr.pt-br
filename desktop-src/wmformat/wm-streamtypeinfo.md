---
title: WM/StreamTypeInfo
description: O atributo WM/StreamTypeInfo contém as informações de configuração para o fluxo especificado no arquivo ASF.
ms.assetid: 4d7f18d4-d76d-4e2e-b8a9-eb96844a2fa1
keywords:
- Formato de mídia do Windows do WM/StreamTypeInfo
topic_type:
- apiref
api_name:
- WM/StreamTypeInfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c410b470e9ddb4ec874325d9c1cca2839c00b1d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104364752"
---
# <a name="wmstreamtypeinfo"></a>WM/StreamTypeInfo

O atributo **WM/StreamTypeInfo** contém as informações de configuração para o fluxo especificado no arquivo asf.

## <a name="global-constant"></a>Constante global

g \_ wszWMStreamTypeInfo

## <a name="data-type"></a>Tipo de Dados

[**WM \_ \_ \_ informações de tipo de fluxo**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_type_info) (**WMT \_ tipo \_ Binary**)

## <a name="remarks"></a>Comentários

Esse atributo se aplica a fluxos específicos. Você não pode recuperar este atributo para o fluxo 0.

Este atributo é somente leitura.

O **WM/StreamTypeInfo** pode ser acessado pelo objeto editor de metadados. Essa é a única maneira de acessar as informações de configuração de fluxo sem abrir o arquivo com o objeto leitor (ou o objeto leitor síncrono).

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




