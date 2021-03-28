---
description: Se você planeja associar um ou mais tipos de arquivo a um novo aplicativo, deve definir um ProgID para cada tipo de arquivo que você deseja associar ao aplicativo.
ms.assetid: 997600C9-5264-44EC-BAEC-CB5CEEA0BD14
title: Como registrar um tipo de arquivo para um novo aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 728cc48075ab1c2631f0a950059da65ae326ae79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967894"
---
# <a name="how-to-register-a-file-type-for-a-new-application"></a>Como registrar um tipo de arquivo para um novo aplicativo

Se você planeja associar um ou mais tipos de arquivo a um novo aplicativo, deve definir um ProgID para cada tipo de arquivo que você deseja associar ao aplicativo.

Para criar um ProgID para cada tipo de arquivo exclusivo que seu aplicativo manipula, use estas etapas.

## <a name="instructions"></a>Instruções

### <a name="step-1"></a>Etapa 1:

Observe que alguns tipos de arquivo têm várias extensões que apontam para o mesmo ProgID; por exemplo:

-   **HKEY \_ CLASSES \_ raiz** \\ **app. jpeg** (seu ProgID)
-   **HKEY \_ CLASSES \_ root** \\ **. jpg** = app. jpeg (os mapeamentos de tipo de arquivo)
-   **HKEY \_ CLASSES \_ raiz** \\ **. jpeg** = app. jpeg

### <a name="step-2"></a>Etapa 2:

Remova os valores de ProgID ao instalar e desinstalar o programa.

### <a name="step-3"></a>Etapa 3:

Deixe os mapeamentos de tipo de arquivo inalterados no momento da desinstalação. Isso funciona porque os mapeamentos de tipo de arquivo são armazenados por usuário em \_ classe HKEY \_ root \\ . ext, e o sistema identifica o caso em que o valor ProgID está ausente e o ignora. Deixar os mapeamentos de tipo de arquivo inalterados evita a necessidade de ter um código condicional que só remove o mapeamento de tipo de arquivo se o valor ainda aponta para o ProgID. É importante evitar isso nos casos em que ele pode ter sido alterado por outro aplicativo e, portanto, não é possível remover facilmente o valor.

### <a name="step-4"></a>Etapa 4:

Especifique um valor exclusivo para a descrição do tipo de arquivo de cada ProgID de tipo de arquivo seguindo um destes procedimentos:

-   Deixe o valor padrão do ProgID vazio, caso em que o sistema usa o arquivo. ext.
-   Forneça um valor localizado via FriendlyTypeName e, para compatibilidade com aplicativos antigos que lêem o registro diretamente, certifique-se de fornecer o valor padrão do ProgID como a descrição do tipo de arquivo (ou seja, use o mesmo valor que é referenciado pelo FriendlyTypeName no recurso em inglês).

## <a name="remarks"></a>Comentários

Se você planeja associar o arquivo a um aplicativo existente, localize um ProgID de aplicativo no registro. Para obter mais informações, consulte [tipos de arquivo](fa-file-types.md).

 

 



