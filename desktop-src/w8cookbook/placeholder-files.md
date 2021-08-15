---
title: Arquivos de espaço reservado
description: Arquivos de espaço reservado
ms.assetid: E14655DA-CEA0-4106-B882-C9E9116FC234
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8891fef6c7fc54a66c093507b1831ab7cc6525ea96d685d06cf6fa8d9ded1e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119452496"
---
# <a name="placeholder-files"></a>Arquivos de espaço reservado

## <a name="platform"></a>Plataforma

**Clientes – Windows 8.1**  
**Servidores – Windows Server 2012** R2  

## <a name="description"></a>Descrição

Os arquivos de espaço reservado permitem aos usuários exibir e gerenciar Microsoft OneDrive arquivos, independentemente da conectividade. Os arquivos de espaço reservado representam o namespace OneDrive, mesmo quando os arquivos não são armazenados em cache localmente. Eles contêm metadados de arquivo e imagens em miniatura de fotos.

## <a name="manifestation"></a>Manifestação

Para usuários e desenvolvedores finais, os arquivos de espaço reservado parecem e se comportam quase da mesma forma que os arquivos locais.

Se seu aplicativo usar a Caixa de Diálogo de Arquivo Comum para enumerar o sistema de arquivos, seu aplicativo não será afetado. Quando o usuário tentar abrir o arquivo na caixa de diálogo comum /file, o conteúdo do arquivo será baixado e será passado para seu aplicativo.

Se seu aplicativo acessar o sistema de arquivos diretamente, seu aplicativo poderá aproveitar os arquivos de espaço reservado usando as diretrizes abaixo.

## <a name="solution"></a>Solução

-   Os espaço reservados são ocultos por convenção com base em atributos
-   Identificar os espaço reservados usando a marca de ID de marca de reparse IO \_ REPARSE \_ TAG ESPAÇO RESERVADO DO \_ \_ ARQUIVO

Use o modelo de dados do shell para um comportamento contínuo:

-   Usar SHCreateItemFromParsingName() para criar um item de shell
-   A vincular ao fluxo usando IShellItem::BindToHandler(STREAM \_ DERIAID)
-   Manipulador de propriedades do usuário para acesso à propriedade (IShellItem2::GetPropertyHandler)
-   Miniatura do shell do usuário para obter imagens em miniatura para os espaço reservados
-   Especifique SupportedProtocols= em sua implementação de verbo se o verbo se vincular \* ao fluxo por meio de BindToHandler


```
#include <winnth> //for IO_REPARSE_TAG_FILE_PLACEHOLDER
//  Helper that indicates this is a 
bool IsFilePlaceholder(WIN32_FIND_DATA const &findData)
{
  return (findData.dwFileAttributes & FILE_ATTRIBUTE_REPARSE_POINT) &&
    (findData.dwReserved0 == IO_REPARSE_TAG_FILE_PLACEHOLDER);
}
bool IsFilePlaceholder(_In_PCWSTR filePath)
{
  bool isPlaceholder = false;
  WIN32_FIND_DATA findData;
  HANDLE hFind = FindFirstFile(filePath, &findData);
  if (hFind ! = INVALID_HANDLE_VALUE)
  {
    isPlaceholder = (findData.dwFileAttributes &    FILE_ATTRIBUTE_REPARSE_POINT) &&
    (findData.dwReserved0 == IO_REPARSE_TAG_FILE_PLACEHOLDER);
    FindClose(hFind);
  }
  Return isPlaceholder;
}
```



 

 




