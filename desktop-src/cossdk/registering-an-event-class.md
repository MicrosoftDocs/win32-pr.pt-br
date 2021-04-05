---
description: Para que os assinantes possam encontrar uma classe de evento e assiná-la, as classes de evento devem ser registradas no catálogo COM+.
ms.assetid: b9d59b9d-52ba-4c71-9226-9cb5b93ec3d4
title: Registrando uma classe de evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89a5968b8cb5981db3eb39c446104e1801a18e2e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646347"
---
# <a name="registering-an-event-class"></a>Registrando uma classe de evento

Para que os assinantes possam encontrar uma classe de evento e assiná-la, as classes de evento devem ser registradas no catálogo COM+. O COM+ requer uma biblioteca de tipos que descreve os métodos e as interfaces de evento para que ele possa corresponder e conectar corretamente assinantes e publicadores. A biblioteca de tipos deve residir ou ser acompanhada por uma DLL de registro automático.

Você pode usar a ferramenta administrativa serviços de componentes ou as funções administrativas do COM+ para registrar uma classe de evento no catálogo COM+.

**Para registrar uma classe de evento com a ferramenta administrativa serviços de componentes**

1.  Crie um novo aplicativo COM+.

2.  Abra a pasta do aplicativo e selecione **componentes**.

3.  No menu **ação** , clique em **novo**. (Você também pode selecionar a pasta **componentes** , clique com o botão direito do mouse, aponte para **novo** e clique em **componente**.)

4.  Clique em **Instalar nova classe (s) de evento**.

5.  Insira o caminho para a DLL de componente da classe de evento.

6.  Clique em **OK**.

A classe de evento é registrada no catálogo COM+ e pode ser localizada por assinantes interessados em obter as informações fornecidas pela classe de evento. Para obter informações sobre como registrar a classe de evento usando as interfaces administrativas do COM+, consulte [**ICOMAdminCatalog:: InstallEventClass**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installeventclass).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registrando uma assinatura](registering-a-subscription.md)
</dt> </dl>

 

 



