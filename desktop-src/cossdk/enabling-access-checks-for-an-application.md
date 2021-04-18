---
description: A execução desta etapa habilita as verificações de acesso do processo ou a segurança total baseada em função, dependendo do nível de segurança que você selecionar e se você habilita a verificação de acesso para componentes individuais.
ms.assetid: 266bdac1-41be-45a5-a8c7-f9c6fe08445c
title: Habilitando verificações de acesso para um aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3d64a32b23467f85c368e088a870ebe5e4d683e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770631"
---
# <a name="enabling-access-checks-for-an-application"></a>Habilitando verificações de acesso para um aplicativo

A execução desta etapa habilita as verificações de acesso do processo ou a segurança total baseada em função, dependendo do nível de segurança que você selecionar e se você habilita a verificação de acesso para componentes individuais.

**Para habilitar verificações de acesso para um aplicativo**

1.  Na árvore de console da ferramenta administrativa serviços de componentes, clique com o botão direito do mouse no aplicativo COM+ para o qual você deseja habilitar as verificações de acesso e clique em **Propriedades**.

2.  Na caixa de diálogo Propriedades do aplicativo, clique na guia **segurança** .

3.  Marque a caixa de seleção **impor verificações de acesso para este aplicativo** .

4.  Clique em **OK**.

> [!Note]  
> A partir do Windows Server 2003, as verificações de acesso são habilitadas por padrão ao criar um aplicativo COM+. As verificações de acesso são habilitadas por padrão no nível do aplicativo e desabilitadas por padrão no nível do componente. Anteriormente, as verificações de acesso foram desabilitadas por padrão no nível do aplicativo e habilitadas por padrão no nível do componente.

 

Depois de habilitar as verificações de acesso, você deve selecionar o nível de segurança apropriado. Consulte [definindo um nível de segurança para verificações de acesso](setting-a-security-level-for-access-checks.md). Além disso, você deve ter certeza de definir funções e adicioná-las ao aplicativo. Se as verificações de acesso estiverem habilitadas, mas nenhuma função tiver sido adicionada, todas as chamadas para o aplicativo falharão. Consulte [definindo funções para um aplicativo](defining-roles-for-an-application.md).

> [!Note]  
> Ao depurar seu aplicativo, pode ser útil desabilitar a segurança para que você possa se concentrar em outros aspectos do comportamento e do design do seu programa.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Atribuindo funções a componentes, interfaces ou métodos](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[Configurando a segurança do Role-Based](configuring-role-based-security.md)
</dt> <dt>

[Definindo funções para um aplicativo](defining-roles-for-an-application.md)
</dt> <dt>

[Habilitando verificações de acesso no nível do componente](enabling-access-checks-at-the-component-level.md)
</dt> <dt>

[Configurando um nível de segurança para verificações de acesso](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



