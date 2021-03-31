---
title: WM/imagem
description: O atributo WM/Picture contém uma imagem relacionada ao conteúdo.
ms.assetid: ec82dfdf-7755-4758-9771-096aac114f78
keywords:
- Formato de mídia do WM/Picture Windows
topic_type:
- apiref
api_name:
- WM/Picture
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ba3f74378112c8e3f58958db8b22c970e8e099
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103916750"
---
# <a name="wmpicture"></a>WM/imagem

O atributo **WM/Picture** contém uma imagem relacionada ao conteúdo.

## <a name="global-constant"></a>Constante global

g \_ wszWMPicture

## <a name="data-type"></a>Tipo de Dados

[**WM \_ PICTURE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture) (**\_ tipo \_ binário WMT**)

## <a name="remarks"></a>Comentários

Esse atributo é compatível com o quadro ID3, APIC. A especificação ID3 para o quadro APIC determina que, embora possa haver qualquer número de quadros APIC associados a um arquivo, apenas um pode ser do tipo 1 e apenas um pode ser do tipo 2. A especificação também indica que a descrição da imagem não pode ter mais de 64 caracteres, mas pode estar vazia.

Os atributos do WM/Picture adicionados com os objetos do Windows Media Format SDK não são validados automaticamente para obedecer às especificações ID3. Você deve adicionar código em seu aplicativo para executar validações se desejar manter a compatibilidade completa com ID3.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> <dt>

[**imagem do WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture)
</dt> </dl>

 

 




