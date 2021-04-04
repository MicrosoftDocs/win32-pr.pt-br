---
title: Efeito de morphology
description: Use o efeito de morphology para limites de borda fino ou THICKEN em uma imagem.
ms.assetid: 4B3CFC51-D556-4729-B433-7307C80291F4
keywords:
- efeitos de morphology
- efeito de didatas
- efeito de Erode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f43cf41810ae0b16c9bc96dd37473a0231fc132c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085905"
---
# <a name="morphology-effect"></a>Efeito de morphology

Use o efeito de morphology para limites de borda fino ou THICKEN em uma imagem. Esse efeito cria um kernel que é 2 vezes os valores de largura e altura que você especificar. Esse efeito centraliza o kernel no pixel que está calculando e retorna o valor máximo no kernel (se dilating) ou no valor mínimo no kernel (se Eroding).

O CLSID para esse efeito é CLSID \_ D2D1Morphology.

## <a name="example-images"></a>Imagens de exemplo

Este exemplo mostra a saída do efeito ao usar o modo Erode.



| Antes                                                     |
|------------------------------------------------------------|
| ![a imagem antes do efeito.](images/default-before.jpg) |
| After (após)                                                      |
| ![a imagem após a transformação.](images/7-morphology.png) |



 


```C++
ComPtr<ID2D1Effect> morphologyEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Morphology, &morphologyEffect);

morphologyEffect->SetInput(0, bitmap);

morphologyEffect->SetValue(D2D1_MORPHOLOGY_PROP_MODE, D2D1_MORPHOLOGY_MODE_ERODE);
morphologyEffect->SetValue(D2D1_MORPHOLOGY_PROP_WIDTH, 14);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(morphologyEffect.Get());
m_d2dContext->EndDraw(); 
```



## <a name="effect-properties"></a>Propriedades do efeito



| Nome de exibição e enumeração de índice                          | Tipo e valor padrão                                                     | Descrição                                                                                                                                                       |
|-------------------------------------------------------------|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mode<br/> \_Modo de \_ prop d2d1 MORPHOLOGY \_<br/>     | \_Modo de MORPHOLOGY d2d1 \_<br/> \_Modo d2d1 \_ MORPHOLOGY \_ Erode<br/> | O modo morphology. Os modos disponíveis são Erode (achatar) e tardia (THICKEN).<br/> Consulte [modos de morphology](#morphology-modes) para obter mais informações.<br/> |
| Largura<br/> \_Largura de \_ prop d2d1 MORPHOLOGY \_<br/>   | UINT<br/> 1<br/>                                               | Tamanho do kernel na direção X. As unidades estão em DIPs. Os valores devem estar entre 1 e 100, inclusive.                                                         |
| Altura<br/> \_Altura de \_ prop d2d1 MORPHOLOGY \_<br/> | UINT<br/> 1<br/>                                               | Tamanho do kernel na direção Y. As unidades estão em DIPs. Os valores devem estar entre 1 e 100, inclusive.                                                         |



 

## <a name="morphology-modes"></a>Modos de morphology



| Nome                           | Descrição                                                    |
|--------------------------------|----------------------------------------------------------------|
| \_Modo d2d1 \_ MORPHOLOGY \_ Erode  | O valor máximo de cada canal RGB no kernel é usado. |
| D2D1 \_ \_ modo MORPHOLOGY \_ | O valor mínimo de cada canal RGB no kernel é usado. |



 

## <a name="output-bitmap"></a>Bitmap de saída

Para o modo de atraso, o tamanho do bitmap de saída aumenta: 

| Requisito | Valor |
|--------------------------|-----------------------------------------|
| Crescimento do bitmap de saída X = | INT (FLOAT (Width) \* ((User DPI)/96))  |
| Crescimento de bitmap de saída Y = | INT (FLOAT (Height) \* ((DPI do usuário)/96)) |



 

Para o modo ERODE, o tamanho do bitmap de saída é reduzido:

| Requisito | Valor |
|--------------------------|------------------------------------------|
| Crescimento do bitmap de saída X = | INT (FLOAT (-Width) \* ((User DPI)/96))  |
| Crescimento de bitmap de saída Y = | INT (FLOAT (-Height) \* ((User DPI)/96)) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte | Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\] |
| Servidor mínimo com suporte | Windows 8 e atualização de plataforma para aplicativos de área de trabalho do Windows 7 \[ \| aplicativos da Windows Store\] |
| parâmetro                   | d2d1effects. h                                                                      |
| Biblioteca                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

