---
description: Uma matriz de associação é uma lista ordenada de locais de registro usados para armazenar informações sobre um tipo de item, incluindo manipuladores, verbos e outros atributos, como o ícone e o nome de exibição do tipo.
title: Matrizes de associação
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 9ECD19CA-833E-4565-A0EF-FB16BF7B3F44
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 75d42a8758e5c6380414c7b93979b4f93cafd013
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090240"
---
# <a name="association-arrays"></a>Matrizes de associação

Uma matriz de associação é uma lista ordenada de locais de registro usados para armazenar informações sobre um tipo de item, incluindo manipuladores, verbos e outros atributos, como o ícone e o nome de exibição do tipo. O Shell usa matrizes de associação para consultar um conjunto predefinido de locais de registro que podem conter informações sobre um item de Shell.

Este tópico é organizado da seguinte maneira:

-   [Sobre matrizes de associação](#about-association-arrays)
-   [Consultando matrizes de associação](#querying-association-arrays)
-   [Trabalhando com matrizes de associação para uma determinada fonte de dados do Shell](#working-with-association-arrays-for-a-particular-shell-data-source)
    -   [Matrizes de associação de fonte de dados do Shell](#shell-data-source-association-arrays)
-   [Recursos adicionais](#additional-resources)
-   [Tópicos relacionados](#related-topics)

## <a name="about-association-arrays"></a>Sobre matrizes de associação

Uma matriz de associação é uma lista ordenada de locais de registro que contêm informações sobre um tipo de item, incluindo manipuladores, verbos e outros atributos, como o ícone e o nome de exibição do tipo. Essas informações sobre o tipo de item podem ser registradas em diferentes níveis de especificidade. Por exemplo, você pode registrar um verbo que será exibido apenas para um tipo de arquivo específico (como. jpg) ou para todos os itens com o mesmo System. Kind (por exemplo, System. Kind = Picture) ou para todos os itens.

O Shell usa matrizes de associação para consultar um conjunto predefinido de locais de registro que podem potencialmente conter informações sobre o item. As APIs da matriz de associação podem ser usadas para recuperar da subchave do registro um único valor que contém as informações solicitadas, com esse valor proveniente da primeira entrada na matriz que a fornece. Por exemplo, o valor de ícone padrão é recuperado dessa forma. A matriz de associação também pode ser usada para recuperar um conjunto de valores que são armazenados nas subchaves do registro. Por exemplo, a lista de verbos é criada a partir dos verbos que são registrados em todas as subchaves.

Depois que o Shell consulta um conjunto predefinido de locais de registro para obter informações sobre um item de Shell, ele coloca os locais do registro em uma matriz na ordem do local mais específico para o mais geral.

Como as matrizes de associação são listas ordenadas, elas fornecem aos desenvolvedores de aplicativos um mecanismo para adicionar informações ao registro que serão retornadas para um tipo específico de item. Da mesma forma, as matrizes de associação permitem que os desenvolvedores de aplicativos adicionem informações ao registro para um grupo específico de itens quando esses itens são registrados em um local mais geral. Essa lógica informa sua decisão sobre o local mais apropriado no registro para armazenar informações sobre itens de Shell.

Em um sistema Windows padrão, um arquivo. jpg tem a seguinte matriz de associação:

-   **HKEY \_ Jpgfile de classes \_ raiz** \\ 
-   **HKEY \_ CLASSES \_ raiz** \\ **SystemFileAssociations** \\ **. jpg**
-   **HKEY \_ Imagem \_ raiz de classes** \\ 
-   **HKEY \_ CLASSES \_ raiz** \\ * *\** _
-   _ *HKEY \_ classes \_ root **\\** AllFilesystemObjects**

Para obter informações sobre como registrar matrizes de associação, consulte [registro de aplicativo](app-registration.md).

## <a name="querying-association-arrays"></a>Consultando matrizes de associação

Há APIs do Shell para recuperar informações de uma variedade de subchaves do registro, da subchave do registro mais específica para um superconjunto das informações em todas as subchaves do registro.

O uso mais comum de uma matriz de associação é consultar um único valor que o Shell retorna do elemento mais específico na matriz que tem as informações solicitadas. O exemplo de código a seguir mostra como fazer isso.


```
IQueryAssociations *pqa;

// pShellItem is assumed to be an existing IShellItem object.
hr = pShellItem->BindToHandler(NULL, BHID_AssociationArray, IID_PPV_ARGS(&pqa));
if (SUCCEEDED(hr))
{
    wchar_t szValue[256];
    DWORD cbValue = sizeof(szValue);      // Count of bytes in the array

    hr = pqa->GetData(0, ASSOCDATA_VALUE, L"InfoTip", szValue, &cbValue);
    if (SUCCEEDED(hr))
    {
        // The "InfoTip" value is used to compute the infotip string from
        // properties of an item.
    }
    pqa->Release();
}
```



As APIs a seguir podem ser usadas para consultar uma matriz de associação ou para construir um objeto [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) de matriz de associação que pode ser consultado:

-   [**AssocCreate**](/windows/desktop/api/Shlwapi/nf-shlwapi-assoccreate) (antes do Windows Vista)
-   [**AssocCreateForClasses**](/windows/desktop/api/Shellapi/nf-shellapi-assoccreateforclasses)
-   [**AssocQueryString**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocquerystringa)

## <a name="working-with-association-arrays-for-a-particular-shell-data-source"></a>Trabalhando com matrizes de associação para uma determinada fonte de dados do Shell

Cada fonte de dados do Shell define a matriz de associação para seus itens. A definição de uma matriz de associação geralmente é uma função do tipo de item. Os implementadores de fonte de dados do Shell devem definir e documentar as matrizes de associação para permitir que os aplicativos estendam o comportamento desses tipos, como para o registro de verbos ou outras informações. Os aplicativos podem estender o comportamento de itens com base na adição de dados às subchaves da matriz de associação, como a adição de verbos para itens.

A fonte de dados do sistema de arquivos cria uma matriz de associação para arquivos com base nas seguintes subchaves de registro e ProgIDs especiais:

-   Se o arquivo tiver um ProgID registrado, a ProgID de **\_ \_ raiz das classes hKey** \\  será usada. Caso contrário, a **\_ \_ raiz de classes hKey** \\ **desconhecida** será usada.
-   A extensão de nome de arquivo é registrada na subchave **HKEY \_ classes \_ raiz** \\ **SystemFileAssociations** \\ *. FileExtension* .
-   ProgIDs especiais são mostrados na tabela a seguir. 

    | ProgID especial                                    | Description                   |
    |---------------------------------------------------|-------------------------------|
    | **HKEY \_ CLASSES \_ raiz** \\ * *\** _                   | Todos os arquivos (não pastas)       |
    | _ *HKEY \_ classes \_ root **\\** AllFilesystemObjects** | Arquivos e pastas do sistema de arquivos |
    | **HKEY \_ Diretório \_ raiz de classes** \\             | Pastas do sistema de arquivos           |
    | **HKEY \_ Pasta \_ raiz de classes** \\                | Contêineres do Shell              |

    

     

### <a name="shell-data-source-association-arrays"></a>Matrizes de associação de fonte de dados do Shell

A lista a seguir representa algumas das matrizes de associação de armazenamento de dados do shell que podem ser usadas para as finalidades descritas neste tópico:

-   **HKEY \_ CLASSES \_ raiz** \\ * *\** _
-   _ *HKEY \_ classes \_ root **\\** AllFilesystemObjects**
-   **HKEY \_ \_Raiz de classes** \\ **Kind.Document**
-   **HKEY \_ Resultados \_ raiz de classes** \\ 
-   **HKEY \_ CLASSES \_ raiz** \\ **SystemFileAssociations** \\ **. docx**
-   **HKEY \_ \_Raiz de classes** \\ **Word.Document. 12**

As matrizes de associação de fonte de dados do shell que podem ser usadas para DBFolder (um armazenamento de dados do shell que representa itens nos resultados da pesquisa e exibições baseadas em consulta) são as seguintes:

-   Unidades
-   Rede
-   RegItems
-   Exemplos:
    -   ContentView
    -   Verbos

Outras matrizes de associação comuns incluem pastas e impressoras.

## <a name="additional-resources"></a>Recursos adicionais

-   Para criar um armazenamento de dados do Shell, consulte [implementando as interfaces de objeto de pasta básica](nse-implement.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[registro de Aplicativo](app-registration.md)
</dt> <dt>

[Tipos de arquivo](fa-file-types.md)
</dt> <dt>

[Como funcionam as associações de arquivo](fa-how-work.md)
</dt> <dt>

[Exibição de conteúdo por tipo de arquivo ou tipo](prophand-content-view.md)
</dt> <dt>

[Verificador de tipo de arquivo](file-type-verifier.md)
</dt> <dt>

[Manipuladores de tipo de arquivo](fa-file-extensions.md)
</dt> <dt>

[Identificadores programáticos](fa-progids.md)
</dt> <dt>

[Tipos observados](fa-perceivedtypes.md)
</dt> </dl>

 

 
