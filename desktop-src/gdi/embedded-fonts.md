---
description: Inserir uma fonte é a técnica de agrupar um documento e as fontes que ele contém em um arquivo para transmissão para outro computador.
ms.assetid: ded409f1-5bd9-411b-b905-fc49c484786a
title: Fontes inseridas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83fb8ab821afa5f44ded05a4a61a53439b8db9fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091187"
---
# <a name="embedded-fonts"></a>Fontes inseridas

Inserir uma fonte é a técnica de agrupar um documento e as fontes que ele contém em um arquivo para transmissão para outro computador. A inserção de uma fonte garante que uma fonte especificada em um arquivo transmitido estará presente no computador que está recebendo o arquivo. Nem todas as fontes podem ser movidas de computador para computador, no entanto, já que a maioria das fontes é licenciada para apenas um computador por vez. Somente fontes TrueType e OpenType podem ser inseridas.

Os aplicativos devem inserir uma fonte em um documento somente quando solicitado por um usuário. Um aplicativo não pode ser distribuído juntamente com documentos que contêm fontes inseridas, nem um aplicativo em si contém uma fonte inserida. Sempre que um aplicativo distribui uma fonte, em qualquer formato, os direitos proprietários do proprietário da fonte devem ser confirmados.

Pode ser uma violação dos direitos proprietários ou do contrato de licença de usuário de um fornecedor de fontes para inserir qualquer fonte em que a inserção não é permitida ou para não observar as diretrizes a seguir sobre a inserção de fontes. A licença de uma fonte pode conceder apenas permissão de leitura/gravação para que uma fonte seja instalada e usada no computador de destino. Ou a licença pode conceder permissão somente leitura. Permissão somente leitura permite que um documento seja exibido e impresso (mas não modificado) pelo computador de destino; documentos com fontes incorporadas somente leitura são somente leitura. Fontes incorporadas somente leitura podem não ser desagrupadas do documento e instaladas no computador de destino.

Um aplicativo pode determinar o status da licença chamando a função [**GetOutlineTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) e examinando o membro **OtmfsType** da estrutura [**OUTLINETEXTMETRIC**](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) . Se o bit 1 de **otmfsType** for definido, a inserção não será permitida para a fonte. Se o bit 1 estiver claro, a fonte poderá ser inserida. Se o bit 2 for definido, a inserção será somente leitura.

Para inserir uma fonte TrueType, um aplicativo pode usar a função [**GetFontData**](/windows/desktop/api/Wingdi/nf-wingdi-getfontdata) para ler o arquivo de fonte. Definir os parâmetros *dwTable* e *dwOffset* de [**GetFontData**](/windows/win32/api/wingdi/nf-wingdi-getfontdata) como 0L e o parâmetro *cbData* como 1L garante que o aplicativo Leia todo o arquivo de fonte desde o início.

Várias funções estão disponíveis para inserir fontes OpenType dependendo da largura do caractere e do local em que os dados da fonte residem. Para inserir uma fonte OpenType Unicode que reside em um contexto de dispositivo, um aplicativo pode usar [**TTEmbedFont**](/windows/desktop/api/T2embapi/nf-t2embapi-ttembedfont). Para inserir uma fonte de UCS-4 OpenType que reside em um contexto de dispositivo, um aplicativo pode usar [**TTEmbedFontEx**](/windows/desktop/api/T2embapi/nf-t2embapi-ttembedfontex). Para inserir uma fonte OpenType Unicode que reside em um arquivo de fonte, um aplicativo pode usar [**TTEmbedFontFromFile**](/windows/desktop/api/T2embapi/nf-t2embapi-ttembedfontfromfilea). Para obter informações adicionais sobre a inserção de fontes OpenType, consulte a [referência de incorporação de fontes](font-embedding-reference.md).

Depois que um aplicativo recupera os dados da fonte, ele pode armazenar os dados com o documento usando qualquer formato aplicável. A maioria dos aplicativos cria um diretório de fontes no documento, listando as fontes inseridas e se a inserção é de leitura/gravação ou somente leitura. Um aplicativo pode usar os membros **otmpStyleName** e **OtmFamilyName** da estrutura [**OUTLINETEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-outlinetextmetrica) para identificar a fonte.

Se o bit somente leitura for definido para a fonte inserida, os aplicativos deverão criptografar os dados da fonte antes de armazená-los com o documento. O método de criptografia não precisa ser complicado; por exemplo, o uso do operador XOR para combinar os dados da fonte com uma constante definida pelo aplicativo é adequado e rápido.

 

 
