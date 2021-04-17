---
title: Constantes DROPEFFECT (OleIdl. h)
description: Representa informações sobre os efeitos de uma operação de arrastar e soltar.
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
ms.openlocfilehash: f2b1888aa028d4e047a9a8ec1f54e2497fa28ce4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105784955"
---
# <a name="dropeffect-constants"></a>Constantes DROPEFFECT

Representa informações sobre os efeitos de uma operação de arrastar e soltar. A função [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) e muitos dos métodos em [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) e [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) usam os valores dessa enumeração.



| Constante/valor                                                                                                                                                                                                                            | Descrição                                                                                                                         |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DROPEFFECT_NONE"></span><span id="dropeffect_none"></span><dl> <dt>**DROPEFFECT \_ NENHUM**</dt> <dt>0</dt> </dl>                | O destino de soltura não pode aceitar os dados.<br/>                                                                                      |
| <span id="DROPEFFECT_COPY"></span><span id="dropeffect_copy"></span><dl> <dt>**DROPEFFECT \_ CÓPIA**</dt> <dt>1</dt> </dl>                | Descartar resultados em uma cópia. Os dados originais são inalterados pela fonte de arrastar.<br/>                                               |
| <span id="DROPEFFECT_MOVE"></span><span id="dropeffect_move"></span><dl> <dt>**DROPEFFECT \_ MOVER**</dt> <dt>2</dt> </dl>                | A origem de arrastar deve remover os dados. <br/>                                                                                     |
| <span id="DROPEFFECT_LINK"></span><span id="dropeffect_link"></span><dl> <dt>**DROPEFFECT \_ LINK**</dt> <dt>4</dt> </dl>                | A origem de arrastar deve criar um link para os dados originais.<br/>                                                                   |
| <span id="DROPEFFECT_SCROLL"></span><span id="dropeffect_scroll"></span><dl> <dt>**DROPEFFECT \_ ROLAR**</dt> <dt>0x80000000</dt> </dl> | A rolagem está prestes a iniciar ou está ocorrendo no momento no destino. Esse valor é usado além dos outros valores.<br/> |



## <a name="remarks"></a>Comentários

Seu aplicativo sempre deve mascarar valores da enumeração **DROPEFFECT** para garantir a compatibilidade com futuras implementações. Atualmente, apenas algumas das posições em um valor **DROPEFFECT** têm significado. No futuro, mais interpretações para os bits serão adicionadas. Arrastar fontes e soltar destinos deve mascarar cuidadosamente esses valores adequadamente antes de comparar. Eles nunca devem comparar um **DROPEFFECT** com relação à cópia, por exemplo, de DROPEFFECT, \_ fazendo o seguinte:

``` syntax
if (dwDropEffect == DROPEFFECT_COPY)... 
```

Em vez disso, o aplicativo sempre deve mascarar o valor ou os valores que estão sendo buscados como usando uma das seguintes técnicas:

``` syntax
if (dwDropEffect & DROPEFFECT_COPY) == DROPEFFECT_COPY)...

if (dwDropEffect & DROPEFFECT_COPY)... 
```

Isso permite a definição de novos efeitos de soltar, enquanto preserva a compatibilidade com versões anteriores com o código existente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>OleIdl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop)
</dt> <dt>

[**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource)
</dt> <dt>

[**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget)
</dt> </dl>

 

 





