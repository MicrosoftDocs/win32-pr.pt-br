---
title: Arquivos de espaço reservado
description: Arquivos de espaço reservado
ms.assetid: E14655DA-CEA0-4106-B882-C9E9116FC234
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93c15037b0daec7a6521a299b6c4587c956e0be3
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "105770312"
---
# <a name="placeholder-files"></a>Arquivos de espaço reservado

## <a name="platform"></a>Plataforma

**Clientes-** Windows 8.1  
**Servidores-** Windows Server 2012 R2  

## <a name="description"></a>Description

Os arquivos de espaço reservado permitem que os usuários exibam e gerenciem arquivos do Microsoft OneDrive independentemente da conectividade. Os arquivos de espaço reservado representam o namespace do OneDrive, mesmo quando os arquivos não são armazenados em cache localmente. Eles contêm metadados de arquivo e imagens em miniatura de fotos.

## <a name="manifestation"></a>Manifestação

Para usuários finais e desenvolvedores, os arquivos de espaço reservado parecem e se comportam quase iguais aos arquivos locais.

Se seu aplicativo usar a caixa de diálogo arquivo comum para enumerar o sistema de arquivos, seu aplicativo não será afetado. Quando o usuário tenta abrir o arquivo da caixa de diálogo do/File comum, o conteúdo do arquivo será baixado e será passado para seu aplicativo.

Se seu aplicativo acessa o sistema de arquivos diretamente, seu aplicativo pode tirar proveito dos arquivos de espaço reservado usando as diretrizes abaixo.

## <a name="solution"></a>Solução

-   Espaços reservados são ocultos por convenção com base em atributos
-   Identificar espaços reservados usando a ID da marca de nova análise e o \_ \_ \_ \_ espaço reservado para arquivo de marca de nova análise

Use o modelo de dados do Shell para um comportamento contínuo:

-   Usar SHCreateItemFromParsingName () para criar um item de Shell
-   Associar ao fluxo usando IShellItem:: BindToHandler (fluxo de BHID \_ )
-   Manipulador de propriedades de usuário para acesso à propriedade (IShellItem2:: GetPropertyHandler)
-   Shell do usuário thumbnailhandler para obter imagens em miniatura para espaços reservados
-   Especifique SupportedProtocols = \* na sua implementação de verbo se o verbo for associado ao fluxo por meio de BindToHandler


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



 

 




