---
description: X opções de formato de arquivo, carregar e salvar.
ms.assetid: 813a2b4b-6577-4cdf-a2e6-e06870638354
title: D3DXF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073887c6cc93754ead01ce379310a9be09edc88f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105796115"
---
# <a name="d3dxf"></a>D3DXF

X opções de formato de arquivo, carregar e salvar.

## <a name="file-formats"></a>Formatos de arquivo

A tabela a seguir especifica o tipo de dados de arquivo:



| \#define para o formato de arquivo     | Valor | Descrição                                                                                    |
|-------------------------------|-------|------------------------------------------------------------------------------------------------|
| \_Binário de FILEFORMATO D3DXF \_     | 0     | Arquivo binário de formato herdado. Consulte [referência de arquivo X (Herdado)](dx9-graphics-reference-x-file.md). |
| Texto do D3DXF \_ FILEformat \_       | 1     | Arquivo de texto.                                                                                     |
| FORMATO de fileD3DXF \_ \_ compactado | 2     | Arquivo compactado. Com esse sinalizador, você também deve especificar o formato binário ou o formato de texto.   |



 

## <a name="file-load-options"></a>Opções de carregamento de arquivo

A tabela a seguir especifica opções de carregamento de arquivo com arquivos. x:



| \#definir                      | Valor | Descrição                |
|-------------------------------|-------|----------------------------|
| D3DXF \_ fileload \_ defile     | 0     | Carregar dados de um arquivo.     |
| D3DXF \_ fileload \_ FROMWFILE    | 1     | Carregar dados de um arquivo.     |
| D3DXF \_ fileload \_ FROMRESOURCE | 2     | Carregar dados de um recurso. |
| D3DXF \_ fileload \_ FROMMEMORY   | 3     | Carregar dados da memória.     |



 

## <a name="file-save-options"></a>Opções de salvamento de arquivo

A tabela a seguir especifica opções de gravação e de carregamento de arquivo com arquivos. x:



| \#definir                 | Valor | Descrição                    |
|--------------------------|-------|--------------------------------|
| D3DXF \_ FILEsalvar \_ ToFile  | 0     | Salvar em um arquivo.                |
| D3DXF \_ FileSave \_ TOWFILE | 1     | Salve em um arquivo de caractere largo. |



 

## <a name="constant-information"></a>Informações constantes



|                          |            |
|--------------------------|------------|
| parâmetro                   | d3dx9xof. h |
| Sistema operacional mínimo | Windows 98 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes de arquivo D3DX X](dx9-graphics-reference-d3dx-x-file-constants.md)
</dt> <dt>

[**D3DXSaveMeshToX**](d3dxsavemeshtox.md)
</dt> </dl>

 

 



