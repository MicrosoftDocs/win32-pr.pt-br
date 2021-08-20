---
title: visão geral do DRM de mídia Windows
description: visão geral do DRM de mídia Windows
ms.assetid: 944b5e0b-649f-4955-8df3-4762726b9893
keywords:
- Windows SDK do formato de mídia, DRM (gerenciamento de direitos digitais)
- Windows SDK do formato de mídia, licenças DRM
- Windows SDK do formato de mídia, licenças para DRM
- DRM (gerenciamento de direitos digitais), sobre
- DRM (gerenciamento de direitos digitais), sobre
- DRM (gerenciamento de direitos digitais), empacotando arquivos de mídia Windows
- DRM (gerenciamento de direitos digitais), empacotando arquivos de mídia Windows
- DRM (gerenciamento de direitos digitais), licenciamento de arquivo protegido
- DRM (gerenciamento de direitos digitais), licenciamento de arquivo protegido
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), lendo arquivos protegidos
- DRM (gerenciamento de direitos digitais), lendo arquivos protegidos
- ASF (Advanced Systems Format), DRM (gerenciamento de direitos digitais)
- ASF (formato de sistemas avançados), DRM (gerenciamento de direitos digitais)
- licenças, DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa6cc882d31873a05361869b9246da1b57ac3d3aebb85073d0b31f24509a615b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846411"
---
# <a name="overview-of-windows-media-drm"></a>visão geral do DRM de mídia Windows

Windows o DRM (Media Digital Rights Management) é um sistema para proteger o conteúdo em arquivos de mídia Windows para que usuários não autorizados não possam acessá-lo. Há três fases para o ciclo de DRM básico: empacotamento, licenciamento e leitura.

## <a name="packaging-windows-media-files"></a>empacotando arquivos de mídia Windows

Windows o DRM de mídia foi projetado para funcionar com Windows arquivos de mídia. um arquivo de mídia Windows é um arquivo que está em conformidade com a especificação ASF (Advanced Systems Format) e contém apenas áudio e vídeo que foram compactados usando os codecs de vídeo e áudio de mídia Windows.

Quando um arquivo ASF é empacotado, uma seção específica de DRM é adicionada ao cabeçalho. O cabeçalho DRM contém uma ID de chave, que identifica o conteúdo para fins de licenciamento e uma URL de aquisição de licença, que é o endereço de uma página da Web que pode emitir licenças para ler o conteúdo protegido. Há muito mais informações que podem ser colocadas no cabeçalho DRM, mas é opcional. O cabeçalho DRM é assinado para que o packager possa ser verificado.

O conteúdo no arquivo ASF é criptografado durante o processo de empacotamento. No entanto, as seguintes informações no arquivo empacotado estão disponíveis até mesmo para clientes que não têm uma licença:

-   Metadados que são armazenados no cabeçalho ASF.
-   Alguns metadados armazenados no cabeçalho DRM (por exemplo, você sempre pode obter a URL de aquisição de licença).

## <a name="licensing-protected-files"></a>Licenciamento de arquivos protegidos

Para que um arquivo empacotado seja lido, uma licença deve ser emitida para o computador cliente. Uma licença é um conjunto de dados que descreve as condições sob as quais os dados nos arquivos protegidos podem ser lidos. Geralmente, uma licença é emitida para um arquivo protegido em resposta ao usuário que está tentando executar alguma operação no arquivo. Também é possível, no entanto, que um emissor de licença entregue licenças a um cliente antes que ele seja explicitamente solicitado. Para obter mais informações sobre licenças, consulte [licenças](licenses.md).

## <a name="reading-data-from-protected-files"></a>Lendo dados de arquivos protegidos

Quando um usuário tenta executar uma operação em um arquivo protegido (reproduzir, gravar em CD, copiar para um dispositivo e assim por diante), o aplicativo deve verificar se há licenças para o conteúdo no computador cliente. Se houver uma licença válida no computador cliente, a operação poderá continuar. Se não houver uma licença para o conteúdo ou se nenhuma licença para o conteúdo que está no computador cliente permitir a ação solicitada, uma licença deverá ser adquirida.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**sobre as APIs estendidas do cliente de DRM de mídia Windows**](about-the-windows-media-drm-client-extended-apis.md)
</dt> </dl>

 

 




