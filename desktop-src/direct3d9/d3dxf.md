---
description: X opções de formato de arquivo, carregar e salvar.
ms.assetid: 813a2b4b-6577-4cdf-a2e6-e06870638354
title: D3DXF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e230fc08ac4d7f8713959f2025f67262046ecea5
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343641"
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
| D3DXF \_ FILELOAD \_ FROMRESOURCE | 2     | Carregar dados de um recurso. |
| D3DXF \_ FILELOAD \_ FROMMEMORY   | 3     | Carregar dados da memória.     |



 

## <a name="file-save-options"></a>Opções de salvar arquivo

A tabela a seguir especifica opções de salvar e carregar arquivos com arquivos .x:



| \#Definir                 | Valor | Descrição                    |
|--------------------------|-------|--------------------------------|
| ARQUIVOS D3DXFAVE \_ \_ TOFILE  | 0     | Salve em um arquivo.                |
| ARQUIVOS D3DXFAVE \_ \_ TOWFILE | 1     | Salve em um arquivo de caractere largo. |



 

## <a name="constant-information"></a>Informações constantes



| Requisito                         | Valor           |
|--------------------------|------------|
| parâmetro                   | d3dx9xof.h |
| Sistema operacional mínimo | Windows 98 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes de arquivo D3DX X](dx9-graphics-reference-d3dx-x-file-constants.md)
</dt> <dt>

[**D3DXSaveMeshToX**](d3dxsavemeshtox.md)
</dt> </dl>

 

 



