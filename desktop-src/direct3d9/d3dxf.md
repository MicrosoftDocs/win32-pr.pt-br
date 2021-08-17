---
description: Opções de formato de arquivo X, carregamento e salvar.
ms.assetid: 813a2b4b-6577-4cdf-a2e6-e06870638354
title: D3DXF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d286ad4cf64133683de026893beb9fa081899e6b170e4b3adb478798eb4b3edf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118096071"
---
# <a name="d3dxf"></a>D3DXF

Opções de formato de arquivo X, carregamento e salvar.

## <a name="file-formats"></a>Formatos de arquivo

A tabela a seguir especifica o tipo de dados de arquivo:



| \#define para Formato de Arquivo     | Valor | Descrição                                                                                    |
|-------------------------------|-------|------------------------------------------------------------------------------------------------|
| BINÁRIO FILEFORMAT D3DXF \_ \_     | 0     | Arquivo binário de formato herddo. Consulte [Referência de arquivo X (herdou).](dx9-graphics-reference-x-file.md) |
| D3DXF \_ FILEFORMAT \_ TEXT       | 1     | Arquivo de texto.                                                                                     |
| FILEFORMAT D3DXF \_ \_ COMPACTADO | 2     | Arquivo compactado. Com esse sinalizador, você também deve especificar o formato binário ou o formato de texto.   |



 

## <a name="file-load-options"></a>Opções de carregamento de arquivo

A tabela a seguir especifica opções de carregamento de arquivo com arquivos .x:



| \#Definir                      | Valor | Descrição                |
|-------------------------------|-------|----------------------------|
| FILELOAD de D3DXF \_ \_ FromFile     | 0     | Carregar dados de um arquivo.     |
| D3DXF \_ FILELOAD \_ FROMWFILE    | 1     | Carregar dados de um arquivo.     |
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

 

 



