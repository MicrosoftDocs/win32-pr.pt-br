---
title: Efeito de borda
description: Use o efeito de borda para estender uma imagem das bordas.
ms.assetid: D3D569F5-9496-4633-93E2-26665FFC3B37
keywords:
- efeito de borda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49fb43ae8b3e9c4eb449a8231f8b4ffcacf7658b
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/28/2021
ms.locfileid: "104506314"
---
# <a name="border-effect"></a>Efeito de borda

Use o efeito de borda para estender uma imagem das bordas. Você pode usar esse efeito para repetir os pixels das bordas da imagem, encapsular os pixels da extremidade oposta da imagem ou espelhar os pixels na borda do bitmap para estender a região do bitmap.

O CLSID para esse efeito é CLSID \_ D2D1Border.

## <a name="example-images"></a>Imagens de exemplo

Os exemplos aqui mostram a saída do efeito de borda usando cada modo. O tamanho de saída é infinito, mas essas imagens de exemplo são cortadas para duas vezes o tamanho.

### <a name="mirror"></a>Espelho



| Antes                                                    |
|-----------------------------------------------------------|
| ![Captura de tela que mostra a imagem antes do efeito.](images/border-before.jpg) |
| After (após)                                                     |
| ![Captura de tela que mostra a imagem após a transformação.](images/10-border.png)   |



 

### <a name="clamp"></a>Clamp



| Antes                                                        |
|---------------------------------------------------------------|
| ![Captura de tela que mostra a imagem antes do efeito de um fixe.](images/border-before.jpg)     |
| After (após)                                                         |
| ![Captura de tela que mostra a imagem após a transformação de um fixe.](images/10-border-clamp.png) |



 

### <a name="wrap"></a>Encapsular



| Antes                                                       |
|--------------------------------------------------------------|
| ![Captura de tela que mostra a imagem antes do efeito de um encapsulamento.](images/border-before.jpg)    |
| After (após)                                                        |
| ![Captura de tela que mostra a imagem após a transformação de um encapsulamento.](images/10-border-wrap.png) |



 


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



## <a name="effect-properties"></a>Propriedades do efeito



| Nome de exibição e enumeração de índice                                  | Descrição                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Modo de borda X<br/> D2D1 \_ Border \_ prop \_ modo de borda \_ \_ X<br/> | O modo de borda na direção X para o efeito. Você pode definir isso como fixe, wrap ou Mirror. Consulte [modos de borda](#edge-modes) para obter mais informações.<br/> O tipo é o modo de borda de borda D2D1 \_ \_ \_ .<br/> O valor padrão é D2D1 \_ borda do modo de borda \_ \_ \_ fixe.<br/> |
| Modo de borda Y<br/> D2D1 \_ Border \_ prop \_ modo de borda \_ \_ Y<br/> | O modo de borda na direção Y para o efeito. Você pode definir isso como fixe, wrap ou Mirror. Consulte [modos de borda](#edge-modes) para obter mais informações.<br/> O tipo é o modo de borda de borda D2D1 \_ \_ \_ .<br/> O valor padrão é D2D1 \_ borda do modo de borda \_ \_ \_ fixe.<br/> |



 

## <a name="edge-modes"></a>Modos de borda



| Nome de exibição e enumeração de índice                            | Descrição                                          |
|---------------------------------------------------------------|------------------------------------------------------|
| Clamp<br/> Modo de borda de \_ borda d2d1 \_ \_ \_ fixe<br/>   | Repete os pixels das bordas da imagem.      |
| Encapsular<br/> \_ \_ \_ Encapsulamento do modo \_ de borda de borda d2d1<br/>     | Usa pixels da borda final oposta da imagem. |
| Espelho<br/> \_Espelho do \_ \_ modo \_ de borda de borda d2d1<br/> | Reflete pixels sobre a borda da imagem.         |



 

## <a name="output-bitmap"></a>Bitmap de saída

O tamanho do bitmap de saída é infinito para todas as entradas, exceto uma imagem de entrada de tamanho 0. Se a altura ou a largura de uma imagem de entrada for 0, o tamanho de saída será 0.

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

 

