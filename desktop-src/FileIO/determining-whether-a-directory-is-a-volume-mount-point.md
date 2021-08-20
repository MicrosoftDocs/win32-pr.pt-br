---
description: Como determinar se um diretório especificado é uma pasta montada.
ms.assetid: b4a2c3d7-8805-41de-b316-592e77076570
title: Determinando se um diretório é uma pasta montada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12c0af53a63f64164604a5f8f22532add3dded1a46d19d96354c0da37e12d4d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150589"
---
# <a name="determining-whether-a-directory-is-a-mounted-folder"></a>Determinando se um diretório é uma pasta montada

É útil determinar se um diretório é uma pasta montada quando, por exemplo, você estiver usando um aplicativo de backup ou de pesquisa limitado a um volume. Esse aplicativo pode acessar informações em vários volumes se você usar funções como [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) para criar pastas montadas para os outros volumes no volume ao qual o aplicativo está limitado. Para obter mais informações, consulte [criando pastas montadas](mounting-and-dismounting-a-volume.md).

Para determinar se um diretório especificado é uma pasta montada, primeiro chame a função [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) e inspecione o sinalizador de **\_ \_ \_ ponto de nova análise de atributo de arquivo** no valor de retorno para ver se o diretório tem um ponto de nova análise associado. Se tiver, use as funções [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) e [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) para obter a marca de nova análise no membro **dwReserved0** da estrutura de [**\_ \_ dados localizar do Win32**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) . Para determinar se o ponto de nova análise é uma pasta montada (e não alguma outra forma de ponto de nova análise), teste se o valor da marca é igual ao valor de **\_ \_ \_ montagem da \_ marca de e/s**. Para obter mais informações, consulte [pontos de nova análise](reparse-points.md).

Para obter o volume de destino de uma pasta montada, use a função [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) .

De maneira semelhante, você pode determinar se um ponto de nova análise é um link simbólico testando se o valor da marca é **a \_ marca de Nova \_ análise \_ de e/s SYMLINK**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Constantes de atributo de arquivo**](file-attribute-constants.md)
</dt> </dl>

 

 



