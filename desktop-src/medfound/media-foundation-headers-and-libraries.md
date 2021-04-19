---
description: Este tópico lista os cabeçalhos e as bibliotecas que definem todas as APIs de Media Foundation.
ms.assetid: 69877842-fafe-408f-b55b-d2ff2277c756
title: Cabeçalhos e bibliotecas do Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3d5412f3f306c6e0d7327c1da1eb4c48bb109a8
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105753051"
---
# <a name="media-foundation-headers-and-libraries"></a>Cabeçalhos e bibliotecas do Media Foundation

Este tópico lista os cabeçalhos e as bibliotecas que definem todas as APIs de Media Foundation.

Para localizar o cabeçalho e a biblioteca de um elemento de API específico, consulte as páginas de referência na [referência de programação de Media Foundation](media-foundation-programming-reference.md).

## <a name="headers"></a>Cabeçalhos

-   codecapi. h
-   D3D11. h
-   d3d9. h
-   d3d9caps. h
-   d3d9types. h
-   DXVA. h
-   dxva2api. h
-   dxvahd. h
-   EVR. h
-   evr9. h
-   mfapi. h
-   mfcaptureengine. h
-   mferrors. h
-   mfidl. h
-   mfmediacapture. h
-   mfmediaengine. h
-   mfmp2dlna. h
-   mfobjects. h
-   mfplat. lib
-   mfplay. h
-   mfreadwrite. h
-   mftransform. h
-   opmapi. h
-   wmcodecdsp. h
-   wmcontainer. h

## <a name="libraries"></a>Bibliotecas

-   dxva2. lib
-   EVR. lib
-   MF. lib
-   mfplat. lib
-   mfplay. lib
-   mfreadwrite. lib
-   mfuuid. lib

## <a name="library-changes-in-windows-7"></a>Alterações de biblioteca no Windows 7

A partir do Windows 7, determinadas funções de Media Foundation são exportadas de diferentes arquivos DLL do que as versões anteriores.

Essas alterações afetam os seguintes arquivos. lib:

-   EVR. lib
-   MF. lib
-   mfplat. lib

Um aplicativo que usa qualquer uma dessas funções deve vincular a um conjunto diferente de arquivos. lib, dependendo da versão do SDK e da plataforma de destino.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Versão do SDK</th>
<th>Bibliotecas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>SDK do Windows para Windows Vista<br/> SDK do Windows para Windows Server 2008<br/></td>
<td>EVR. lib<br/> MF. lib<br/> mfplat. lib<br/></td>
</tr>
<tr class="even">
<td>SDK do Windows para o Windows 7</td>
<td>Se a plataforma de destino for o Windows Vista ou o Windows Server 2008, vincule as seguintes bibliotecas:<br/>
<ul>
<li>evr_vista. lib</li>
<li>mf_vista. lib</li>
<li>mfplat_vista. lib</li>
</ul>
Se a plataforma de destino for o Windows 7 ou posterior, vincule as seguintes bibliotecas:<br/>
<ul>
<li>EVR. lib</li>
<li>MF. lib</li>
<li>mfplat. lib</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="additional-info-on-helper-functions"></a>Informações adicionais sobre funções auxiliares

O MFPlat.dll do Windows 8 é um componente do sistema operacional Microsoft Windows. Ele tem várias funções incluídas no módulo.

O MFPlat implementa a funcionalidade auxiliar para alocação de memória de nível baixo, PEPS de agendamento de operação e abstrações de acesso a arquivos Win32. Para ser mais específico, ele fornece suporte para o seguinte:

-   Alocando e inicializando buffers de memória (conhecidos como "amostras") e auxiliares para simplificar o gerenciamento de seus tempos de vida
-   funções de cópia de dados eficientes para buffers de memória
-   Alocando e inicializando FIFOs de operação (conhecidos como "eventos")
-   Implementando um objeto Clock simples
-   Implementando um invólucro de arquivo Win32
-   Alocando e inicializando matrizes de buffers de memória para CPUs e GPUs

Se o método [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) for executado com sucesso, o MFPlat fornecerá a seguinte funcionalidade de fila de trabalho:

-   suporte interno a itens de e/s (conforme usado pelas bibliotecas de soquete e invólucro de arquivo do Win32)
-   fornecendo uma matriz de filas de trabalho multi-threaded com suporte de prioridade de thread
-   suporte a itens de trabalho, itens de timer e itens de espera por meio das filas de trabalho

O MFPlat fornece a funcionalidade auxiliar para localizar e criar transformações de mídia e fontes de mídia registradas no sistema, bem como criar e manipular tipos de mídia, embora MFPlat em si não possa criar a mídia real nem reproduzi-la novamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o Media Foundation](about-the-media-foundation-sdk.md)
</dt> </dl>

 

 




