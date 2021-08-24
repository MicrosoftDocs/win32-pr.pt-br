---
description: Diretrizes para o registro de filtros
ms.assetid: 05945937-9e01-4930-ae95-1931a711b55e
title: Diretrizes para o registro de filtros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 221cadf6fb4806a2fa5c5b2cc4fd9abf423cec426ec23cd76b0bc642080852af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905356"
---
# <a name="guidelines-for-registering-filters"></a>Diretrizes para o registro de filtros

as informações de registro de filtro determinam como o filtro Graph Manager funciona durante [Conexão inteligente](intelligent-connect.md). portanto, ele afeta todos os aplicativos escritos para DirectShow, não apenas aqueles que usarão seu filtro. Você deve certificar-se de que o filtro se comporta corretamente, seguindo estas diretrizes.

1.  Você precisa dos dados de filtro no registro? Para muitos filtros personalizados, não há motivo para tornar o filtro visível para o mapeador de filtro ou para o enumerador de dispositivo do sistema. Contanto que você registre a DLL, seu aplicativo pode criar o filtro usando **CoCreateInstance**. Nesse caso, basta omitir a estrutura do [**\_ filtro AMOVIESETUP**](amoviesetup-filter.md) do modelo de fábrica. (Uma desvantagem é que o filtro não estará visível no GraphEdit. Para contornar isso, você pode criar uma categoria de "teste" privada usando o método [**IFilterMapper2:: createcategory**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-createcategory) . Você só deve fazer isso para compilações de depuração.)
2.  Escolha a categoria de filtro correta. a categoria padrão de "filtros de DirectShow" é para filtros de uso geral. Sempre que apropriado, Registre seu filtro em uma categoria mais específica. Quando o [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) pesquisa um filtro, ele ignora qualquer categoria cujo mérito é mérito \_ \_ não \_ usa ou menos. As categorias não destinadas à reprodução normal têm um mérito baixo.
3.  Evite especificar MEDIATYPE \_ None, MEDIASUBTYPE \_ None ou GUID \_ NULL nas informações de [**\_ MediaType de AMOVIESETUP**](amoviesetup-mediatype.md) para um PIN. **IFilterMapper2** trata esses caracteres como curingas, o que pode retardar o processo de criação de gráficos.
4.  Escolha o valor de mérito mais baixo possível. Aqui estão algumas diretrizes:

    | Tipo de filtro                                                                                       | Mérito recomendado                                                                                   |
    |------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
    | Renderizador padrão                                                                                     | MÉRITO \_ preferencial. Para os tipos de mídia padrão, no entanto, um renderizador personalizado nunca deve ser o padrão. |
    | Renderizador não padrão                                                                                 | O \_ mérito \_ não \_ usa nem mérito \_ improvável                                                              |
    | MUX                                                                                                  | MÉRITO \_ \_ não \_ use                                                                                 |
    | Decodificador                                                                                              | MÉRITO \_ normal                                                                                       |
    | Spitter, analisador                                                                                      | MÉRITO \_ normal ou inferior                                                                              |
    | Filtro de finalidade especial; qualquer filtro criado diretamente pelo aplicativo                       | MÉRITO \_ \_ não \_ use                                                                                 |
    | Capturar                                                                                              | MÉRITO \_ \_ não \_ use                                                                                 |
    | Filtro de "fallback"; por exemplo, o [filtro conversor de espaço de cor](color-space-converter-filter.md) | MÉRITO \_ improvável                                                                                     |

    

     

    Se você estiver dando a um filtro um mérito de mérito não \_ \_ \_ usar, considere se precisa registrar essas informações em primeiro lugar. (Consulte o item 1.)

5.  não registre um filtro na categoria "filtros de DirectShow" que aceita RGB de 24 bits. O filtro interferirá com o filtro de conversor de espaço de cor.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[como registrar filtros de DirectShow](how-to-register-directshow-filters.md)
</dt> </dl>

 

 



