---
title: Constantes DROPEFFECT (OleIdl.h)
description: Representa informações sobre os efeitos de uma operação do tipo "arrastar e soltar".
ms.assetid: d8e46899-3fbf-4012-8dd3-67fa627526d5
topic_type:
- apiref
api_name:
- DROPEFFECT_NONE
- DROPEFFECT_COPY
- DROPEFFECT_MOVE
- DROPEFFECT_LINK
- DROPEFFECT_SCROLL
api_location:
- OleIdl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05c9a4fa961b0da2e654d4672392104b95e718bbb176167c7bb715c39f25cfc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736948"
---
# <a name="dropeffect-constants"></a>Constantes DROPEFFECT

Representa informações sobre os efeitos de uma operação do tipo "arrastar e soltar". A [**função DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) e muitos dos métodos em [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) e [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) usam os valores dessa enumeração.



| Constante/valor                                                                                                                                                                                                                            | Descrição                                                                                                                         |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DROPEFFECT_NONE"></span><span id="dropeffect_none"></span><dl> <dt>**DROPEFFECT \_ NONE**</dt> <dt>0</dt> </dl>                | O destino de soltar não pode aceitar os dados.<br/>                                                                                      |
| <span id="DROPEFFECT_COPY"></span><span id="dropeffect_copy"></span><dl> <dt>**DROPEFFECT \_ CÓPIA**</dt> <dt>1</dt> </dl>                | Soltar resultados em uma cópia. Os dados originais não são tocados pela origem do arrastar.<br/>                                               |
| <span id="DROPEFFECT_MOVE"></span><span id="dropeffect_move"></span><dl> <dt>**DROPEFFECT \_ MOVE**</dt> <dt>2</dt> </dl>                | A origem do arrastar deve remover os dados. <br/>                                                                                     |
| <span id="DROPEFFECT_LINK"></span><span id="dropeffect_link"></span><dl> <dt>**DROPEFFECT \_ LINK**</dt> <dt>4</dt> </dl>                | Arrastar fonte deve criar um link para os dados originais.<br/>                                                                   |
| <span id="DROPEFFECT_SCROLL"></span><span id="dropeffect_scroll"></span><dl> <dt>**DROPEFFECT \_ SCROLL**</dt> <dt>0x80000000</dt> </dl> | A rolagem está prestes a iniciar ou está ocorrendo no destino. Esse valor é usado além dos outros valores.<br/> |



## <a name="remarks"></a>Comentários

Seu aplicativo sempre deve mascarar valores da **enumeração DROPEFFECT** para garantir a compatibilidade com implementações futuras. Atualmente, apenas algumas das posições em um **valor DROPEFFECT** têm significado. No futuro, mais interpretações para os bits serão adicionadas. As fontes de arrastar e soltar destinos devem mascarar cuidadosamente esses valores adequadamente antes de comparar. Eles nunca devem comparar **um DROPEFFECT com,** digamos, DROPEFFECT \_ COPY fazendo o seguinte:

``` syntax
if (dwDropEffect == DROPEFFECT_COPY)... 
```

Em vez disso, o aplicativo sempre deve mascarar o valor ou os valores que estão sendo procurados como usando uma das seguintes técnicas:

``` syntax
if (dwDropEffect & DROPEFFECT_COPY) == DROPEFFECT_COPY)...

if (dwDropEffect & DROPEFFECT_COPY)... 
```

Isso permite a definição de novos efeitos de soltar, preservando a compatibilidade com o código existente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>OleIdl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Dodragdrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop)
</dt> <dt>

[**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource)
</dt> <dt>

[**Idroptarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget)
</dt> </dl>

 

 





