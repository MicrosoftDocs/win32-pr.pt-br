---
title: Componentes do Windows instalados sob demanda
description: Componentes do Windows instalados sob demanda
ms.assetid: 14865DD7-167C-462C-B85A-BD07C929D7B8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09d2c3c3fee1cd12d7b12900e41dc006badcf53f
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104008496"
---
# <a name="windows-components-installed-on-demand"></a>Componentes do Windows instalados sob demanda

## <a name="platform"></a>Plataforma

**Clientes-** Windows 8.1  







## <a name="description"></a>Descrição

Dois componentes do Windows serão instalados sob demanda no Windows 8.1: DirectPlay e NTVDM. Esses componentes são listados em componentes opcionais no nó "componentes herdados". Esses componentes são instalados localmente como parte do sistema operacional e compactados como componentes opcionais. Quando um aplicativo referencia ou chama um desses componentes (normalmente na primeira inicialização do aplicativo), a instalação é disparada automaticamente. Os usuários serão notificados de que o componente será instalado e deverão confirmar a ação para continuar. A elevação será necessária para que isso tenha sucesso se o usuário não for um administrador. Após a instalação inicial, o usuário não precisa executar nenhuma outra ação para usar o componente novamente.

## <a name="manifestation"></a>Manifestação

Quando um aplicativo referencia ou chama um componente herdado em componentes opcionais (na primeira inicialização), o aplicativo será suspenso e a caixa de diálogo recurso sob demanda será aberta, solicitando permissão do usuário para instalar o componente. Se os usuários clicarem em OK, eles também poderão ver um prompt de elevação em que eles deverão inserir suas credenciais. O componente será instalado e o aplicativo será retomado.

## <a name="mitigation"></a>Atenuação

Para impedir que os recursos da interface do usuário sob demanda sejam abertos, você pode pré-instalar o DirectPlay e o NTVDM usando o DISM ou a interface do usuário de componentes opcionais.

## <a name="solution"></a>Solução

É altamente recomendável evitar a referência ou a chamada de componentes que foram listados como componentes opcionais herdados no Windows em versões futuras do seu aplicativo. Os componentes opcionais herdados incluirão apenas componentes mais antigos e menos usados que possam causar problemas de desempenho e segurança para os usuários.

## <a name="tests"></a>Testes

Nenhuma acomodações de teste adicional é necessária para compatibilidade. É importante estar ciente de que essa caixa de diálogo será exibida quando o componente opcional for chamado ou referenciado e essa instalação exigir elevação.

 

 




