---
title: Objetos de dados do servidor
description: A API do SDO (Server Data Objects) possibilita configurar e administrar programaticamente um sistema que executa o NPS.
ms.assetid: 9d159e15-f534-4ab1-9641-db70064beb51
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d51c4a8b04b9da6994daa4941d255f0d74f68ea858d4a3909ed9ecc1ae28514
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128406"
---
# <a name="server-data-objects"></a>Objetos de dados do servidor

> [!Note]  
> O IAS (Serviço de Autenticação da Internet) foi renomeado como NPS (Servidor de Políticas de Rede) a partir do Windows Server 2008. O conteúdo deste tópico se aplica a IAS e NPS. Em todo o texto, o NPS é usado para se referir a todas as versões do serviço, incluindo as versões originalmente conhecidas como IAS.

 

A API do SDO (Server Data Objects) possibilita configurar e administrar programaticamente um sistema que executa o NPS. Usando o SDO, um desenvolvedor também pode escrever aplicativos que administram perfis e políticas de acesso remoto. As políticas e perfis de acesso remoto são usados pelo Serviço de Roteamento e Acesso Remoto (RRAS), bem como pelo NPS para determinar se um cliente remoto tem permissão para se conectar a um NAS (servidor de acesso à rede).

A API SDO é aplicável em qualquer ambiente que use NPS ou Políticas de Acesso Remoto.

Com a API SDO, um desenvolvedor pode manipular qualquer elemento da configuração do NPS acessível por meio da interface do usuário do NPS.

A API SDO também possibilita definir ou recuperar qualquer um dos valores acessíveis por meio da página de propriedades de configurações discada pelo usuário.

A API SDO é composta por interfaces COM. Cada uma das interfaces na API SDO herda da interface [**COM IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) A interface **IDispatch** permite que os desenvolvedores chamem os métodos de interface SDO do Visual Basic ou de qualquer cliente de Automação, bem como do C/C++.

Os desenvolvedores também podem chamar a API SDO de linguagens de script, como VBScript. No entanto, como o VBScript está limitado ao uso apenas de parâmetros de tipo VARIANT, nem toda a funcionalidade do SDO está disponível.

## <a name="in-this-section"></a>Nesta seção

[Visão geral](/windows/desktop/Nps/sdo-about-server-data-objects)

Informações gerais sobre a API de Objetos de Dados do Servidor.

[Usando](/windows/desktop/Nps/sdo-using-server-data-objects)

Código de exemplo que demonstra como usar a API de Objetos de Dados do Servidor.

[Referência](/windows/desktop/Nps/sdo-server-data-objects-reference)

Documentação dos tipos e interfaces enumerados que compõem a API de Objetos de Dados do Servidor.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Servidor de Política de Rede (Serviço de Autenticação da Internet)](portal.md)
</dt> <dt>

[Serviço de Acesso Remoto](/windows/desktop/RRAS/portal)
</dt> </dl>

 

 