---
title: Visão geral do DRM do Windows Media
description: Visão geral do DRM do Windows Media
ms.assetid: 944b5e0b-649f-4955-8df3-4762726b9893
keywords:
- SDK do Windows Media Format, DRM (gerenciamento de direitos digitais)
- SDK do Windows Media Format, licenças DRM
- SDK do Windows Media Format, licenças para DRM
- DRM (gerenciamento de direitos digitais), sobre
- DRM (gerenciamento de direitos digitais), sobre
- DRM (gerenciamento de direitos digitais), empacotando arquivos de mídia do Windows
- DRM (gerenciamento de direitos digitais), empacotando arquivos de mídia do Windows
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
ms.openlocfilehash: d14cb76fcf61346aab9bd68746afc7e50a2f146d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105793282"
---
# <a name="overview-of-windows-media-drm"></a>Visão geral do DRM do Windows Media

O Windows Media Digital Rights Management (DRM) é um sistema para proteger o conteúdo em arquivos de mídia do Windows para que usuários não autorizados não possam acessá-lo. Há três fases para o ciclo de DRM básico: empacotamento, licenciamento e leitura.

## <a name="packaging-windows-media-files"></a>Empacotando Arquivos de mídia do Windows

O DRM do Windows Media foi projetado para funcionar com arquivos de mídia do Windows. Um arquivo de mídia do Windows é um arquivo que está em conformidade com a especificação ASF (Advanced Systems Format) e contém apenas áudio e vídeo que foram compactados usando os codecs de áudio e vídeo do Windows Media.

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

[**Sobre as APIs estendidas do cliente DRM do Windows Media**](about-the-windows-media-drm-client-extended-apis.md)
</dt> </dl>

 

 




