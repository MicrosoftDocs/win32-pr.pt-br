---
title: Usando o compartilhamento de largura de banda
description: Usando o compartilhamento de largura de banda
ms.assetid: 1df61a3a-d34a-447e-a7ee-d5d409e7c4fa
keywords:
- SDK do Windows Media Format, compartilhamento de largura de banda
- compartilhamento de largura de banda, sobre
- perfis, compartilhamento de largura de banda
- fluxos, compartilhamento de largura de banda
- compartilhamento de largura de banda, interface IWMProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 298c690b484a8b4b5990aacd5d525867da8923c0
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104365757"
---
# <a name="using-bandwidth-sharing"></a>Usando o compartilhamento de largura de banda

Você pode usar objetos de compartilhamento de largura de banda para especificar que determinados fluxos, quando combinados, não usarão mais largura de banda do que o especificado. As informações em um objeto de compartilhamento de largura de banda não são geradas nem verificadas pelo gravador nem usadas pelo leitor para qualquer coisa.

Quando um arquivo é gravado com informações de compartilhamento de largura de banda em seu perfil, os dados são armazenados em sua seção de cabeçalho. Você pode usar a interface [**IWMProfile**](iwmprofile.md) no leitor para verificar se há informações de compartilhamento de largura de banda quando o arquivo é reproduzido.

Cada objeto de compartilhamento de largura de banda é definido por duas configurações. A primeira é a largura de banda, conforme definido por uma largura de banda e uma janela de buffer. A segunda configuração é um tipo de compartilhamento de largura de banda, que pode ser exclusivo ou parcial. O compartilhamento de largura de banda exclusivo significa que os fluxos constituintes são reproduzidos um de cada vez, enquanto os fluxos parciais são entregues simultaneamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IWMProfile**](iwmprofile.md)
</dt> <dt>

[**IWMProfile3::AddBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-addbandwidthsharing)
</dt> <dt>

[**IWMProfile3::CreateNewBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewbandwidthsharing)
</dt> <dt>

[**IWMProfile3::GetBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharing)
</dt> <dt>

[**IWMProfile3::GetBandwidthSharingCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharingcount)
</dt> <dt>

[**Trabalhando com perfis**](working-with-profiles.md)
</dt> </dl>

 

 




