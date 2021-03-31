---
description: O tipo de aplicativo que você cria determina a qual formato de persistência de tinta dar suporte.
ms.assetid: bd0a4382-f014-4f03-990d-d2f96aa76ab8
title: Escolhendo quais formatos dar suporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 891fa1c21dd3178e925deab27525afa7fa70fa22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171867"
---
# <a name="choosing-which-formats-to-support"></a>Escolhendo quais formatos dar suporte

O tipo de aplicativo que você cria determina a qual formato de persistência de tinta dar suporte.

## <a name="single-ink-object-applications"></a>Aplicativos de objeto de tinta única

Os aplicativos cujos documentos contêm apenas tinta devem usar o formato serializado da tinta (ISF). Eles devem ser capazes de copiar e colar o formato serializado de tinta (ISF). Um exemplo disso é um aplicativo para desenho ou anotação. Esses aplicativos podem usar os métodos [**ClipboardCopy**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopy)e [**ClipboardPaste**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardpaste) .

## <a name="complex-applications"></a>Aplicativos complexos

Os aplicativos cujos documentos contêm outro conteúdo, como texto, devem copiar HTML com arquivos reforçada Graphics Interchange Format (GIF), além de ISF. O próprio HTML deve ser gerado pelo aplicativo, embora as interfaces de programação de aplicativo (APIs) do Tablet PC gerem arquivos GIF. Esses aplicativos também devem ser capazes de copiar e colar ISF para interoperabilidade com os aplicativos descritos acima.

## <a name="rtf"></a>RTF

Um aplicativo deve ser capaz de produzir Rich Text Format (RTF) se a interoperabilidade com o Microsoft Word 2002 ou outros aplicativos herdados for necessária.

## <a name="mime-support"></a>Suporte a MIME

A tabela a seguir lista os cabeçalhos MIME (Multipurpose Internet Mail Extensions) sugeridos e extensões de arquivo para a tinta que é persistida em arquivos usando o ISF ou GIF. Esses valores são encontrados na enumeração [**PersistenceFormat**](/windows/desktop/api/msinkaut/ne-msinkaut-inkpersistenceformat) .



| Formato de persistência            | Cabeçalho MIME                                                                                    | Extensão do arquivo            |
|-------------------------------|------------------------------------------------------------------------------------------------|---------------------------|
| **Base64Gif**                 | Tipo de conteúdo: application/x-MS-Ink Content-transcodificação-Encoding: Base64<br/>                | Não aplicável<br/> |
| **Base64InkSerializedFormat** | Tipo de conteúdo: Content-Type: image/gif; formato = conteúdo de tinta-transferência-codificação: Base64<br/> | Não aplicável<br/> |
| **Gifs**                       | Tipo de conteúdo: aplicativo/x-MS-Ink<br/>                                                  | .gif<br/>           |
| **InkSerializedFormat**       | Tipo de conteúdo: Content-Type: image/gif; formato = tinta<br/>                                   | . ISF<br/>           |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Enumeração PersistenceFormat**](/windows/desktop/api/msinkaut/ne-msinkaut-inkpersistenceformat)
</dt> </dl>

 

 




