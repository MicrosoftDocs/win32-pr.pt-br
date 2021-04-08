---
description: Os idiomas ocidentais são definidos como Inglês (Reino Unido), inglês (Estados Unidos), francês, alemão e espanhol.
ms.assetid: d4728506-7484-4c4c-a5ae-e98d699f7e76
title: Factos para idiomas ocidentais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de98cfce0203a2a3a94509d6586c1596390ca16b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010533"
---
# <a name="factoids-for-western-languages"></a>Factos para idiomas ocidentais

Os idiomas ocidentais são definidos como Inglês (Reino Unido), inglês (Estados Unidos), francês, alemão e espanhol. Os formatos em cada factor mostrado na tabela a seguir são específicos para o reconhecedor de cada idioma. Por exemplo, o facto de **telefone** é diferente em cada idioma. Além disso, cada factor é específico para um reconhecedor específico. Por exemplo, o facto de **telefone** francês pode ser usado apenas com o reconhecedor francês.

> [!Note]  
> Além dos seguintes factos, todos os idiomas usam as opções listadas em [factos comuns em todos os idiomas](factoids-common-across-languages.md).

 



| Facto              | Definição                                                                                                                                                                                                                                                                                                                                                                                                           | Exemplos                                                                                                                                                                                                                                                            |
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Filename**         | Define o Bias para um caminho de nome de arquivo. O nome não pode incluir os caracteres<br/> /" < > \|<br/> Os caracteres \* e? estão incluídos neste factoid para habilitar a pesquisa. Além disso, os caracteres estendidos têm suporte em idiomas europeus.<br/>                                                                                                                                                    | c:<br/> \\\\\\nome de arquivo DirectoryName<br/> \\\\directory1 \\ Directory2 \\ nome do arquivo<br/> \\\\DirectoryName \\ \* .\*<br/> nome do arquivo.?<br/> myfile.doc<br/>                                                                                |
| **SystemDictionary** | Habilita apenas o dicionário do sistema. Isso será útil se um aplicativo consultar se uma palavra está no dicionário do sistema. Defina o factoname como **SystemDictionary** e chame o método [**IsStringSupported**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-isstringsupported) .<br/>                                                                                                                                                 | O modelo de idioma padrão inclui a gramática para o idioma, bem como o dicionário do sistema. Esse factor ajusta o reconhecimento em direção apenas às palavras que ocorrem no dicionário do sistema. Cada idioma tem seu próprio dicionário do sistema.<br/>                   |
| **Palavras**         | Habilita somente a lista de palavras. Se o factor for definido como lista de **palavras** , mas não for atribuída a nenhum [**InkRecognizerContext**](inkrecognizercontext-class.md) ([RecognizerContext](/previous-versions/ms552546(v=vs.100)) no código gerenciado), o dicionário do usuário será usado. Para obter mais informações sobre listas de palavras e dicionários, consulte [usando dicionários de aplicativos](using-application-dictionaries.md).<br/> | Esse factor ajusta o reconhecedor para retornar apenas palavras na lista de palavras. Por exemplo, para permitir que o usuário insira uma cor em um formulário, você pode usar esse factor e uma lista de palavras que contenha "verde", "vermelho", "azul", "branco" e outras cores.<br/> |



 

As seguintes combinações de factors têm suporte apenas para idiomas ocidentais. Não há suporte para outras combinações de factors nesta versão das APIs (interfaces de programação de aplicativo) da plataforma do Tablet PC. Essas combinações de factor empregam um operador **or** lógico, portanto, a entrada pode corresponder a qualquer um dos factos na expressão.



| Combinação de factor     | Definição                                                                   |
|-------------------------|------------------------------------------------------------------------------|
| **Webwordlist**         | O facto **da Web** ou a lista de palavras.<br/>                             |
| **EmailWordList**       | O facto de **email** ou a lista de palavras.<br/>                           |
| **FilenameWebWordList** | O **nome do arquivo** ou o factor **da Web** ou a lista de palavras.<br/> |



 

Os tópicos a seguir mostram os formatos com suporte para cada idioma ocidental.

-   [Factos em inglês (Mundial)](english--worldwide--factoids.md)
-   [Factos em inglês (Estados Unidos)](english--united-states--factoids.md)
-   [Factos em francês](french-factoids.md)
-   [Factos de alemão](german-factoids.md)
-   [Refactos de espanhol](spanish-factoids.md)

 

