---
description: Se você planeja associar um ou mais tipos de arquivo a um novo aplicativo, defina um ProgID para cada tipo de arquivo que deseja associar ao aplicativo.
ms.assetid: 997600C9-5264-44EC-BAEC-CB5CEEA0BD14
title: Como registrar um tipo de arquivo para um novo aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9de165d378d27c6891b681f95da7242b026844bd7734709ebd272c06edf40e3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859656"
---
# <a name="how-to-register-a-file-type-for-a-new-application"></a>Como registrar um tipo de arquivo para um novo aplicativo

Se você planeja associar um ou mais tipos de arquivo a um novo aplicativo, defina um ProgID para cada tipo de arquivo que deseja associar ao aplicativo.

Para criar um ProgID para cada tipo de arquivo exclusivo que seu aplicativo trata, use estas etapas.

## <a name="instructions"></a>Instruções

### <a name="step-1"></a>Etapa 1:

Observe que alguns tipos de arquivo têm várias extensões que apontam para o mesmo ProgID; por exemplo:

-   **HKEY \_ CLASSES \_ ROOT** \\ **App.jpeg** (seu ProgID)
-   **HKEY \_ CLASSES \_ ROOT** \\ **.jpg** = App.jpeg (os mapeamentos de tipo de arquivo)
-   **HKEY \_ CLASSES \_ ROOT** \\ **.jpeg** = App.jpeg

### <a name="step-2"></a>Etapa 2:

Remova os valores progID ao instalar e desinstalar o programa.

### <a name="step-3"></a>Etapa 3:

Deixe os mapeamentos de tipo de arquivo inalterados no momento da desinstalação. Isso funciona porque os mapeamentos de tipo de arquivo são armazenados por usuário em CLASSES HKEY ROOT .ext e o sistema identifica o caso em que o valor ProgID está ausente e o \_ \_ \\ ignora. Deixar mapeamentos de tipo de arquivo inalterados evita a necessidade de ter um código condicional que apenas remova o mapeamento de tipo de arquivo se o valor ainda aponta para o ProgID. É importante evitar isso em casos em que ele possa ter sido alterado por outro aplicativo e, portanto, você não pode remover facilmente o valor.

### <a name="step-4"></a>Etapa 4:

Especifique um valor exclusivo para a descrição de tipo de arquivo de cada tipo de arquivo ProgID fazendo um dos seguintes:

-   Deixe o valor padrão do ProgID vazio, caso em que o sistema usa o arquivo .ext.
-   Forneça um valor localizado por meio de FriendlyTypeName e, para compatibilidade com aplicativos antigos que leem diretamente o Registro, forneça o valor padrão do ProgID como a descrição do tipo de arquivo (ou seja, use o mesmo valor referenciado pelo FriendlyTypeName no recurso em inglês).

## <a name="remarks"></a>Comentários

Se você planeja associar o arquivo a um aplicativo existente, localize um ProgID de aplicativo no Registro. Para obter mais informações, consulte [Tipos de arquivo](fa-file-types.md).

 

 



