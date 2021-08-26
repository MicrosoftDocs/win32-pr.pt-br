---
title: Efeito de compensação de DPI
description: Use o efeito de compensação de DPI para ajustar automaticamente um bitmap de entrada para corresponder ao DPI do contexto. Isso é útil para situações em que um bitmap é criado ou carregado em um DPI diferente da tela.
ms.assetid: EA8AD89B-A710-468F-A6F3-474DA29586F1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38f1390825087cabb9ee1bec65f2708990757ff25f08e71140be5be0fc6ae11e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967106"
---
# <a name="dpi-compensation-effect"></a>Efeito de compensação de DPI

Use o efeito de compensação de DPI para ajustar automaticamente um bitmap de entrada para corresponder ao DPI do contexto. Isso é útil para situações em que um bitmap é criado ou carregado em um DPI diferente da tela.

O CLSID para esse efeito é CLSID \_ D2D1DpiCompensation.

## <a name="effect-properties"></a>Propriedades do efeito



| Nome de exibição e enumeração de índice                                                       | Descrição                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interpolação<br/> \_Modo de \_ \_ interpolação de prop d2d1 DPICOMPENSATION \_<br/> | O modo de interpolação que o efeito usa para dimensionar a imagem.<br/> O tipo é o \_ \_ modo de interpolação d2d1 DPICOMPENSATION \_ .<br/> O valor padrão é D2D1 \_ DPICOMPENSATION \_ modo de interpolação \_ \_ linear.<br/>                  |
| Bordermode<br/> \_Modo de \_ borda de prop d2d1 DPICOMPENSATION \_ \_<br/>               | O modo usado para calcular a borda da imagem, suave ou difícil. Consulte [modos de borda](https://www.bing.com/search?q=Border+modes) para obter mais informações. <br/> O tipo é o \_ modo de borda d2d1 \_ .<br/> O valor padrão é \_ Soft Mode do modo de borda d2d1 \_ \_ .<br/> |
| InputDpi<br/> \_Dpi de entrada d2d1 DPICOMPENSATION \_ prop \_ \_<br/>                   | O DPI da imagem de entrada.<br/> O tipo é FLOAT.<br/> O valor padrão é 96.0 f.<br/>                                                                                                                                    |



 

## <a name="interpolation-modes"></a>Modos de interpolação



| Enumeração                                                       | Descrição                                                                                                                                                                                          |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ DPICOMPENSATION \_ modo de interpolação \_ \_ mais próximo \_     | Amostra o ponto único mais próximo e o usa. Esse modo usa menos tempo de processamento, mas gera a imagem de qualidade mais baixa.                                                                           |
| \_Modo de \_ interpolação d2d1 DPICOMPENSATION \_ \_ linear                | Usa uma amostra de quatro pontos e uma interpolação linear. Esse modo usa mais tempo de processamento do que o modo de vizinho mais próximo, mas gera uma imagem de qualidade mais alta.                                           |
| \_Modo de \_ interpolação d2d1 DPICOMPENSATION \_ \_ cúbico                 | Usa um kernel cúbico de 16 amostras para interpolação. Esse modo usa o maior tempo de processamento, mas gera uma imagem de qualidade mais alta.                                                                        |
| \_Modo de \_ interpolação d2d1 DPICOMPENSATION com \_ \_ várias \_ amostras \_ lineares | Usa quatro amostras lineares em um único pixel para suavização de multialias de borda. Esse modo é bom para reduzir horizontalmente por pequenas quantidades em imagens com poucos pixels.                                              |
| \_Modo de \_ interpolação d2d1 DPICOMPENSATION \_ \_ ANISOTROPIC           | Usa a filtragem de anisotropic para exemplificar um padrão de acordo com a forma transformada do bitmap.                                                                                                     |
| \_Modo de \_ interpolação d2d1 DPICOMPENSATION de \_ \_ alta \_ qualidade \_ cúbico  | Usa um kernel cúbico de tamanho variável de alta qualidade para executar uma imagem diminuir se downscaling estiver envolvido na matriz de transformação. Em seguida, usa o modo de interpolação cúbica para a saída final. |



 

> [!Note]  
> Se você não selecionar um modo, o efeito assume o padrão de D2D1 \_ DPICOMPENSTION \_ modo de interpolação \_ \_ linear.

 

## <a name="border-modes"></a>Modos de borda



| Nome                     | Descrição                                                                                                 |
|--------------------------|-------------------------------------------------------------------------------------------------------------|
| \_Modo de borda d2d1 \_ \_ Soft | Os pixels fora dos limites de entrada são gerados pelo [efeito de borda de espelho](border.md). <br/> |
| \_Modo de borda d2d1 \_ \_ Hard | Os pixels fora dos limites de entrada são pretos transparentes.<br/>                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte | Windows 8 e atualização de plataforma para aplicativos de área de trabalho Windows 7 \[ \| Windows aplicativos da loja\] |
| Servidor mínimo com suporte | Windows 8 e atualização de plataforma para aplicativos de área de trabalho Windows 7 \[ \| Windows aplicativos da loja\] |
| Cabeçalho                   | d2d1effects. h                                                                      |
| Biblioteca                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

