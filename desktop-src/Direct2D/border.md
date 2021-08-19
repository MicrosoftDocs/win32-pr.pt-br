---
title: Efeito de borda
description: Use o efeito de borda para estender uma imagem das bordas.
ms.assetid: D3D569F5-9496-4633-93E2-26665FFC3B37
keywords:
- efeito de borda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ce125a96730ee59f63b18cfd1a08abd2432af6f3fdc6b5f06cfc2e9272a7a3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928976"
---
# <a name="border-effect"></a>Efeito de borda

Use o efeito de borda para estender uma imagem das bordas. Você pode usar esse efeito para repetir os pixels das bordas da imagem, envolver os pixels da extremidade oposta da imagem ou espelhar os pixels na borda do bitmap para estender a região do bitmap.

O CLSID para esse efeito é CLSID \_ D2D1Border.

## <a name="example-images"></a>Imagens de exemplo

Os exemplos aqui mostram a saída do efeito de borda usando cada modo. O tamanho da saída é infinito, mas essas imagens de exemplo são cortadas para o dobro do tamanho.

### <a name="mirror"></a>Espelho



| Antes                                                    |
|-----------------------------------------------------------|
| ![Captura de tela que mostra a imagem antes do efeito.](images/border-before.jpg) |
| Depois                                                     |
| ![Captura de tela que mostra a imagem após a transformação.](images/10-border.png)   |



 

### <a name="clamp"></a>Clamp



| Antes                                                        |
|---------------------------------------------------------------|
| ![Captura de tela que mostra a imagem antes do efeito de um fixador.](images/border-before.jpg)     |
| Depois                                                         |
| ![Captura de tela que mostra a imagem após a transformação de um fixador.](images/10-border-clamp.png) |



 

### <a name="wrap"></a>Encapsular



| Antes                                                       |
|--------------------------------------------------------------|
| ![Captura de tela que mostra a imagem antes do efeito de um wrap.](images/border-before.jpg)    |
| Depois                                                        |
| ![Captura de tela que mostra a imagem após a transformação para um wrap.](images/10-border-wrap.png) |



 


```C++
ComPtr<ID2D1Effect> borderEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Border, &borderEffect);

borderEffect->SetInput(0, bitmap);
borderEffect->SetValue(D2D1_BORDER_PROP_EDGE_MODE_X, D2D1_BORDER_EDGE_MODE_MIRROR);
borderEffect->SetValue(D2D1_BORDER_PROP_EDGE_MODE_Y, D2D1_BORDER_EDGE_MODE_MIRROR);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(borderEffect.Get());
m_d2dContext->EndDraw(); 
```



## <a name="effect-properties"></a>Propriedades de efeito



| Nome de exibição e enumeração de índice                                  | Descrição                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Modo de borda X<br/> D2D1 \_ BORDER \_ PROP \_ EDGE \_ MODE \_ X<br/> | O modo de borda na direção X para o efeito. Você pode definir isso como fixação, quebra ou espelho. Consulte [Modos de borda para](#edge-modes) obter mais informações.<br/> O tipo é D2D1 \_ BORDER \_ EDGE \_ MODE.<br/> O valor padrão é D2D1 \_ BORDER \_ EDGE MODE \_ \_ FIX.<br/> |
| Modo de borda Y<br/> D2D1 \_ BORDER \_ PROP \_ EDGE \_ MODE \_ Y<br/> | O modo de borda na direção Y para o efeito. Você pode definir isso como fixação, quebra ou espelho. Consulte [Modos de borda para](#edge-modes) obter mais informações.<br/> O tipo é D2D1 \_ BORDER \_ EDGE \_ MODE.<br/> O valor padrão é D2D1 \_ BORDER \_ EDGE MODE \_ \_ FIX.<br/> |



 

## <a name="edge-modes"></a>Modos de borda



| Nome de exibição e enumeração de índice                            | Descrição                                          |
|---------------------------------------------------------------|------------------------------------------------------|
| Clamp<br/> FIXE NO MODO DE BORDA D2D1 \_ \_ BORDER \_ \_ EDGE<br/>   | Repete os pixels das bordas da imagem.      |
| Encapsular<br/> D2D1 \_ BORDER \_ EDGE \_ MODE \_ WRAP<br/>     | Usa pixels da borda de extremidade oposta da imagem. |
| Espelho<br/> D2D1 \_ BORDER \_ EDGE \_ MODE \_ MIRROR<br/> | Reflete pixels sobre a borda da imagem.         |



 

## <a name="output-bitmap"></a>Bitmap de saída

O tamanho do bitmap de saída é infinito para todas as entradas, exceto uma imagem de entrada de tamanho 0. Se a altura ou a largura de uma imagem de entrada for 0, o tamanho da saída será 0.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte | Windows 8 e Atualização de Plataforma para Windows 7 aplicativos da área de trabalho \[ \| Windows Store\] |
| Servidor mínimo com suporte | Windows 8 e Atualização de Plataforma para Windows 7 aplicativos da área de trabalho \[ \| Windows Store\] |
| Cabeçalho                   | d2d1effects.h                                                                      |
| Biblioteca                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

