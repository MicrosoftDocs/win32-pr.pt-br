---
title: Armazenamento assíncrono
description: O armazenamento assíncrono aprimora a especificação de armazenamento estruturado COM para dar suporte ao download assíncrono de objetos de armazenamento em redes de alta latência e de link lento, como a Internet.
ms.assetid: 12b97059-2c8c-4712-8a76-03c3ce7094a0
keywords:
- Armazenamento estruturado Strctd STG, armazenamento assíncrono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39dd1d739223fb07c72de6c63ee173c316a132e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454234"
---
# <a name="asynchronous-storage"></a>Armazenamento assíncrono

O armazenamento assíncrono aprimora a especificação de armazenamento estruturado COM para dar suporte ao download assíncrono de objetos de armazenamento em redes de alta latência e de link lento, como a Internet. O armazenamento assíncrono permite que aplicativos novos e herdados usem arquivos compostos para processar com eficiência seu conteúdo quando acessados por meio de protocolos de Internet existentes. Uma única solicitação para um servidor de World Wide Web dispara o download de objetos aninhados contidos em uma página da Web, eliminando a necessidade de solicitar cada objeto separadamente. Um mecanismo de download e acesso assíncrono permite que um aplicativo processe a primeira página de dados antes que todos os dados tenham sido recebidos. A ordem exata na qual os elementos de uma página se torna disponível pode ser especificada pelo editor da Web e não depende de fatores aleatórios de topologia de rede e disponibilidade do servidor.

O armazenamento assíncrono funciona junto com monikers assíncronos para fornecer comportamento de ligação assíncrona completo. Para obter mais informações sobre monikers assíncronos, consulte o Software Development Kit do Microsoft ActiveX. Um moniker assíncrono específico de protocolo dispara a operação de associação e configura os componentes necessários. No caso da Internet, esse moniker seria um que pode analisar uma URL para associar a um objeto ou armazenamento. Se o destino da operação de associação for um objeto persistente, a chamada para [**IMoniker:: BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) retornará um objeto de armazenamento assíncrono.

> [!Note]  
> A versão atual dos monikers de URL da Microsoft não oferece suporte ao armazenamento assíncrono.

 

Um cliente de moniker assíncrono solicita a vinculação assíncrona implementando um objeto de retorno de chamada de status de ligação e registrando-o com o contexto de associação. O objeto de retorno de chamada de status de ligação expõe a interface [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) , que permite ao cliente especificar preferências de associação e receber notificações de progresso e disponibilidade de dados globais durante o curso de uma operação de vinculação. A implementação de arquivo composto assíncrono fornece um ponto de conexão para [**IProgressNotify**](/windows/win32/api/objidl/nn-objidl-iprogressnotify), que os clientes podem usar para receber notificações de disponibilidade específicas em fluxos individuais.

 

 