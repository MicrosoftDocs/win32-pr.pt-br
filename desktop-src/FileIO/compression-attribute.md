---
description: Em um volume do sistema de arquivos NTFS, cada arquivo e diretório têm um atributo de compactação.
ms.assetid: 8aca120c-22a7-4dc8-a921-dfcec1277452
title: Atributo de compactação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2e8e86eebe919476851f35f77cf10d6a07035d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837426"
---
# <a name="compression-attribute"></a>Atributo de compactação

Em um volume do sistema de arquivos NTFS, cada arquivo e diretório têm um *atributo de compactação*. Outros sistemas de arquivos também podem implementar um atributo de compactação para arquivos e diretórios individuais.

Você pode determinar se um sistema de arquivos dá suporte a um atributo de compactação para arquivos e diretórios chamando a função [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) e examinando o sinalizador de bit de **\_ \_ compactação do arquivo de arquivo** .

Use a função [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) ou [**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) para determinar o atributo de compactação de um arquivo ou diretório.

Se o atributo de compactação de um arquivo for definido (**atributo de arquivo \_ \_ compactado**), todos os dados no arquivo serão compactados. Se o atributo estiver claro, nenhum dos dados no arquivo será compactado. Não há nenhum estado parcialmente compactado de uma perspectiva de programação no modo de usuário; o atributo de compactação é um indicador booliano simples do estado de compactação.

O atributo de compactação de um diretório fornece um atributo de compactação padrão para arquivos e subdiretórios recém-criados. Quando você chama [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) ou [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) para criar um novo arquivo ou diretório, o novo arquivo ou diretório herda o atributo de compactação de seu diretório pai.

Para modificar o **atributo \_ \_ compactado atributo de arquivo** para um arquivo ou diretório, você deve usar a função [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) com o código de controle de [**\_ \_ compactação Set fsctl**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Constantes de atributo de arquivo**](file-attribute-constants.md)
</dt> </dl>

 

 
