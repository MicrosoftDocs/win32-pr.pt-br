---
title: Windows componentes instalados sob demanda
description: Windows componentes instalados sob demanda
ms.assetid: 14865DD7-167C-462C-B85A-BD07C929D7B8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 765768d2e16005ca0a465b53f076c64c6a30f31b8739113954ccc11959c8e0c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028794"
---
# <a name="windows-components-installed-on-demand"></a>Windows componentes instalados sob demanda

## <a name="platform"></a>Plataforma

**clientes-** Windows 8.1  







## <a name="description"></a>Descrição

dois componentes Windows serão instalados sob demanda no Windows 8.1: DirectPlay e NTVDM. Esses componentes são listados em componentes opcionais no nó "componentes herdados". Esses componentes são instalados localmente como parte do sistema operacional e compactados como componentes opcionais. Quando um aplicativo referencia ou chama um desses componentes (normalmente na primeira inicialização do aplicativo), a instalação é disparada automaticamente. Os usuários serão notificados de que o componente será instalado e deverão confirmar a ação para continuar. A elevação será necessária para que isso tenha sucesso se o usuário não for um administrador. Após a instalação inicial, o usuário não precisa executar nenhuma outra ação para usar o componente novamente.

## <a name="manifestation"></a>Manifestação

Quando um aplicativo referencia ou chama um componente herdado em componentes opcionais (na primeira inicialização), o aplicativo será suspenso e a caixa de diálogo recurso sob demanda será aberta, solicitando permissão do usuário para instalar o componente. Se os usuários clicarem em OK, eles também poderão ver um prompt de elevação em que eles deverão inserir suas credenciais. O componente será instalado e o aplicativo será retomado.

## <a name="mitigation"></a>Atenuação

Para impedir que os recursos da interface do usuário sob demanda sejam abertos, você pode pré-instalar o DirectPlay e o NTVDM usando o DISM ou a interface do usuário de componentes opcionais.

## <a name="solution"></a>Solução

é altamente recomendável evitar a referência ou a chamada de componentes que foram listados como componentes opcionais herdados em Windows em versões futuras do seu aplicativo. Os componentes opcionais herdados incluirão apenas componentes mais antigos e menos usados que possam causar problemas de desempenho e segurança para os usuários.

## <a name="tests"></a>Testes

Nenhuma acomodações de teste adicional é necessária para compatibilidade. É importante estar ciente de que essa caixa de diálogo será exibida quando o componente opcional for chamado ou referenciado e essa instalação exigir elevação.

 

 




