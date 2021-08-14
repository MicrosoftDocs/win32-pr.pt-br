---
title: Usando o compartilhamento de largura de banda
description: Usando o compartilhamento de largura de banda
ms.assetid: 1df61a3a-d34a-447e-a7ee-d5d409e7c4fa
keywords:
- Windows SDK de Formato de Mídia, compartilhamento de largura de banda
- compartilhamento de largura de banda,sobre
- perfis, compartilhamento de largura de banda
- fluxos, compartilhamento de largura de banda
- compartilhamento de largura de banda, interface IWMProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7259ddf441a4e32eb7eb4aea19a52d633c6aacd3a27ad6d392e4fea41c3f4fa8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845152"
---
# <a name="using-bandwidth-sharing"></a>Usando o compartilhamento de largura de banda

Você pode usar objetos de compartilhamento de largura de banda para especificar que determinados fluxos, quando combinados, não usarão mais largura de banda do que o especificado. As informações em um objeto de compartilhamento de largura de banda não são geradas nem verificadas pelo autor nem usadas pelo leitor para nada.

Quando um arquivo é gravado com informações de compartilhamento de largura de banda em seu perfil, os dados são armazenados em sua seção de header. Você pode usar a interface [**IWMProfile**](iwmprofile.md) no leitor para verificar se há informações de compartilhamento de largura de banda quando o arquivo é reproduzir.

Cada objeto de compartilhamento de largura de banda é definido por duas configurações. A primeira é a largura de banda, conforme definido por uma largura de banda e uma janela de buffer. A segunda configuração é um tipo de compartilhamento de largura de banda, que pode ser exclusivo ou parcial. O compartilhamento de largura de banda exclusivo significa que os fluxos constituintes são transmitidos um por vez, enquanto parcial significa que os fluxos são entregues simultaneamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IWMProfile Interface**](iwmprofile.md)
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

 

 




