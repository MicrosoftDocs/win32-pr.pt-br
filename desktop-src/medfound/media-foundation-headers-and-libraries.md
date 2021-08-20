---
description: Este tópico lista os headers e bibliotecas que definem todas as APIs Media Foundation dados.
ms.assetid: 69877842-fafe-408f-b55b-d2ff2277c756
title: Media Foundation e bibliotecas do Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6db7650c98f6491fa6db4010273475b4bd103a2
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467463"
---
# <a name="media-foundation-headers-and-libraries"></a>Media Foundation e bibliotecas do Media Foundation

Este tópico lista os headers e bibliotecas que definem todas as APIs Media Foundation dados.

Para encontrar o header e a biblioteca de um elemento de API específico, consulte as páginas de referência [Media Foundation Referência de Programação.](media-foundation-programming-reference.md)

## <a name="headers"></a>Cabeçalhos

-   codecapi.h
-   d3d11.h
-   d3d9.h
-   d3d9caps.h
-   d3d9types.h
-   dxva.h
-   dxva2api.h
-   dxvahd.h
-   evr.h
-   evr9.h
-   mfapi.h
-   mfcaptureengine.h
-   mferrors.h
-   mfidl.h
-   mfmediacapture.h
-   mfmediaengine.h
-   mfmp2dlna.h
-   mfobjects.h
-   mfplat.lib
-   mfplay.h
-   mfreadwrite.h
-   mftransform.h
-   opmapi.h
-   wmcodecdsp.h
-   wmcontainer.h

## <a name="libraries"></a>Bibliotecas

-   dxva2.lib
-   evr.lib
-   mf.lib
-   mfplat.lib
-   mfplay.lib
-   mfreadwrite.lib
-   mfuuid.lib

## <a name="library-changes-in-windows-7"></a>Alterações na biblioteca Windows 7

A partir do Windows 7, determinadas Media Foundation funções são exportadas de arquivos DLL diferentes das versões anteriores.

Essas alterações afetam os seguintes arquivos .lib:

-   evr.lib
-   mf.lib
-   mfplat.lib

Um aplicativo que usa qualquer uma dessas funções deve vincular a um conjunto diferente de arquivos .lib, dependendo da versão do SDK e da plataforma de destino.




| Versão do SDK | Bibliotecas | 
|-------------|-----------|
| Windows SDK para Windows Vista<br /> Windows SDK para Windows Server 2008<br /> | evr.lib<br /> mf.lib<br /> mfplat.lib<br /> | 
| Windows SDK para Windows 7 | Se a plataforma de destino for Windows Vista ou Windows Server 2008, vincule as seguintes bibliotecas:<br /><ul><li>evr_vista.lib</li><li>mf_vista.lib</li><li>mfplat_vista.lib</li></ul>Se a plataforma de destino for Windows 7 ou posterior, vincule as seguintes bibliotecas:<br /><ul><li>evr.lib</li><li>mf.lib</li><li>mfplat.lib</li></ul> | 




 

## <a name="additional-info-on-helper-functions"></a>Informações adicionais sobre funções auxiliares

O Windows 8 MFPlat.dll é um componente do sistema operacional Microsoft Windows. Ele tem várias funções incluídas no módulo.

O MFPlat implementa a funcionalidade auxiliar para alocação de memória de baixo nível, FIFOs de agendamento de operação e abstrações de acesso ao arquivo win32. Para ser mais específico, ele fornece suporte para o seguinte:

-   alocar e inicializar buffers de memória (conhecidos como 'exemplos') e auxiliares para simplificar o gerenciamento de seus tempos de vida
-   funções eficientes de cópia de dados para buffers de memória
-   alocando e inicializando FIFOs (conhecidos como 'eventos')
-   implementando um objeto de relógio simples
-   implementando um wrapper de arquivo win32
-   alocando e inicializando matrizes de buffers de memória para CPUs e GPUs

Se o [**método MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) for bem-sucedido, o MFPlat fornece a seguinte funcionalidade de fila de trabalho:

-   dando suporte interno a itens de E/S (conforme usado pelo wrapper de arquivo win32 e bibliotecas de soquete)
-   fornecendo uma matriz de filas de trabalho multithread com suporte à prioridade de thread
-   dando suporte a itens de trabalho, itens de temporizador e itens de espera por meio das filas de trabalho

O MFPlat fornece funcionalidade auxiliar para localizar e criar transformaçãos de mídia e fontes de mídia registradas no sistema e criar e manipular tipos de mídia, embora o próprio MFPlat não possa criar a mídia real nem reproduzi-la.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o Media Foundation](about-the-media-foundation-sdk.md)
</dt> </dl>

 

 




