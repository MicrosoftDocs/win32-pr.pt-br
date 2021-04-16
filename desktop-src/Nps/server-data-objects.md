---
title: Objetos de dados do servidor
description: A API de SDO (objetos de dados do servidor) possibilita a configuração e a administração programaticamente de um sistema que executa o NPS.
ms.assetid: 9d159e15-f534-4ab1-9641-db70064beb51
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eebd0f837f9a8a36af1eb9118189015e677e2af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105779597"
---
# <a name="server-data-objects"></a>Objetos de dados do servidor

> [!Note]  
> O IAS (serviço de autenticação da Internet) foi renomeado como NPS (servidor de políticas de rede) a partir do Windows Server 2008. O conteúdo deste tópico aplica-se ao IAS e ao NPS. Em todo o texto, o NPS é usado para fazer referência a todas as versões do serviço, incluindo as versões originalmente chamadas de IAS.

 

A API de SDO (objetos de dados do servidor) possibilita a configuração e a administração programaticamente de um sistema que executa o NPS. Usando o SDO, um desenvolvedor também pode escrever aplicativos que administrem perfis e políticas de acesso remoto. As políticas de acesso remoto e os perfis são usados pelo RRAS (serviço de roteamento e acesso remoto), bem como pelo NPS, para determinar se um cliente remoto tem permissão para se conectar a um NAS (servidor de acesso à rede).

A API de SDO é aplicável em qualquer ambiente que usa políticas de acesso remoto ou NPS.

Com a API de SDO, um desenvolvedor pode manipular qualquer elemento da configuração do NPS acessível por meio da interface do usuário do NPS.

A API SDO também torna possível definir ou recuperar qualquer um dos valores acessíveis por meio da página de propriedades configurações de discagem do usuário.

A API de SDO é composta por interfaces COM. Cada uma das interfaces na API de SDO herda da interface COM [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . A interface **IDispatch** permite que os desenvolvedores chamem os métodos de interface SDO de Visual Basic ou de qualquer cliente de automação, bem como do C/C++.

Os desenvolvedores também podem chamar a API de SDO de linguagens de script, como o VBScript. No entanto, como o VBScript é limitado ao uso apenas de parâmetros de tipo VARIANT, nem toda a funcionalidade de SDO está disponível.

## <a name="in-this-section"></a>Nesta seção

[Visão geral](/windows/desktop/Nps/sdo-about-server-data-objects)

Informações gerais sobre a API de objetos de dados do servidor.

[Usando](/windows/desktop/Nps/sdo-using-server-data-objects)

Código de exemplo que demonstra como usar a API de objetos de dados do servidor.

[Referência](/windows/desktop/Nps/sdo-server-data-objects-reference)

Documentação dos tipos enumerados e interfaces que compõem a API de objetos de dados do servidor.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Servidor de políticas de rede (serviço de autenticação da Internet)](portal.md)
</dt> <dt>

[Serviço de acesso remoto](/windows/desktop/RRAS/portal)
</dt> </dl>

 

 