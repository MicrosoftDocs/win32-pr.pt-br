---
title: WinRM C++ API
description: As Windows interfaces de Gerenciamento Remoto podem ser usadas para obter dados ou gerenciar recursos em um computador remoto. Essa API destina-se principalmente ao uso interno. É recomendável usar a API do Shell do Cliente WinRM sempre que possível.
ms.assetid: e50075a1-cb43-4bd6-9bbf-6b715fde6a3a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71c6039dde1884f2b4b7aa9801fbbd26bb0e10b9a5353dffb5096ba66461d1d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742942"
---
# <a name="winrm-c-api"></a>WinRM C++ API

As Windows interfaces de Gerenciamento Remoto podem ser usadas para obter dados ou [*gerenciar recursos*](windows-remote-management-glossary.md) em um computador remoto. Essa API destina-se principalmente ao uso interno. É recomendável usar a [API do Shell do Cliente WinRM](client-shell-api.md) sempre que possível. As interfaces correspondem de perto à [API de Script WinRM](winrm-scripting-api.md).

As interfaces WinRM que herdam diretamente **de IDispatch** têm um objeto de script correspondente. Para obter mais informações, consulte a [API de Script WinRM](winrm-scripting-api.md).

Para aplicativos multithread, o WinRM não dá suporte a threads separados que acessam o mesmo [**objeto IWSMAN.**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)

As interfaces a seguir são fornecidas pelo WinRM.

<dl> <dt>

<span id="IWSMan"></span><span id="iwsman"></span><span id="IWSMAN"></span>[**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)
</dt> <dd>

Fornece métodos e propriedades usados para criar uma nova sessão e gerenciar uma sessão estabelecida. [**WSMan**](wsman.md) é o objeto de script correspondente.

</dd> <dt>

<span id="IWSManEx"></span><span id="iwsmanex"></span><span id="IWSMANEX"></span>[**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)
</dt> <dd>

Fornece métodos e propriedades usados para criar um [**novo IWSManResourceLocator.**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) Esse método está disponível para o objeto de script [**WSMan.**](wsman.md)

</dd> <dt>

<span id="IWSManConnectionOptions"></span><span id="iwsmanconnectionoptions"></span><span id="IWSMANCONNECTIONOPTIONS"></span>[**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions)
</dt> <dd>

Define o nome de usuário e a senha usados para conexões remotas. [**ConnectionOptions é**](connectionoptions.md) o objeto de script correspondente.

</dd> <dt>

<span id="IWSManSession"></span><span id="iwsmansession"></span><span id="IWSMANSESSION"></span>[**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)
</dt> <dd>

Define as operações de rede e as propriedades disponíveis para a sessão. [**Session**](session.md) é o objeto de script correspondente.

</dd> <dt>

<span id="IWSManEnumerator"></span><span id="iwsmanenumerator"></span><span id="IWSMANENUMERATOR"></span>[**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator)
</dt> <dd>

Representa uma coleção de resultados retornados da enumeração de um recurso. [**Enumerador**](enumerator.md) é o objeto de script correspondente.

</dd> <dt>

<span id="IWSManResourceLocator"></span><span id="iwsmanresourcelocator"></span><span id="IWSMANRESOURCELOCATOR"></span>[**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)
</dt> <dd>

Fornece o caminho para um recurso. Você pode usar um [**objeto IWSManResourceLocator em vez**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) de um [*URI de recurso*](windows-remote-management-glossary.md) em operações de objeto [**session.**](session.md) [**ResourceLocator**](resourcelocator.md) é o objeto de script correspondente.

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Referência de gerenciamento remoto](windows-remote-management-reference.md)
</dt> </dl>

 

 




