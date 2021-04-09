---
title: Host do protocolo de autenticação extensível
description: Saiba mais sobre o host EAP (Extensible Authentication Protocol). Consulte requisitos de tempo de execução e exiba recursos adicionais disponíveis.
ms.assetid: caaef367-2952-44fc-ac4c-f0db6387850e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f007435c43969ad0f195b0a6a1e697ab817d9c4
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "104085020"
---
# <a name="extensible-authentication-protocol-host"></a>Host do protocolo de autenticação extensível

## <a name="purpose"></a>Finalidade


O EAPHost é um componente de rede do Microsoft Windows que fornece uma infraestrutura EAP (Extensible Authentication Protocol) para a autenticação de implementações de protocolo "suplicante", como [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) e [ponto a ponto](https://go.microsoft.com/fwlink/p/?linkid=83919) (PPP). Ele também permite a autenticação com tecnologias "autenticador", como o Microsoft Network Policy Server (NPS). Ao contrário do servidor IAS anterior ([RADIUS](/windows/desktop/Nps/ias-about-internet-authentication-service)), o NPS dá suporte à NAP ( [proteção de acesso à rede](/windows/desktop/NAP/network-access-protection-start-page) ).


As APIs do EAPHost permitem que os aplicativos se autentiquem usando o serviço EAPHost e forneçam um modelo para o desenvolvimento de métodos de autenticação em conformidade para uso com o EAPHost.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

As APIs do EAPHost têm suporte apenas no Windows Vista e sistemas operacionais posteriores.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o EAPHost](about-eap-host.md)
</dt> <dt>

[Usando o EAPHost](using-eap-host.md)
</dt> <dt>

[Referência da API EAPHost](eaphost-api-reference.md)
</dt> </dl>

 

 