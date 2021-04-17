---
description: Habilitando verificações de acesso no nível do componente
ms.assetid: b9ff5296-9076-4492-833c-7402b7090f8f
title: Habilitando verificações de acesso no nível do componente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5da2de5f9d2f4f2d39f43330c8320c0bb0218bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105797609"
---
# <a name="enabling-access-checks-at-the-component-level"></a>Habilitando verificações de acesso no nível do componente

Se seu aplicativo inclui um componente que não precisa de verificações de segurança, você pode optar por desabilitar as verificações de função para esse componente para melhorar o desempenho. Ou durante a depuração, pode ser útil desabilitar a segurança para que você possa se concentrar em outros aspectos da funcionalidade do programa.

Por padrão, quando você instala um componente, as verificações de acesso no nível de componente são habilitadas. No entanto, isso só terá efeito quando as [verificações de acesso no nível do aplicativo](enabling-access-checks-for-an-application.md) estiverem habilitadas e quando o nível de [segurança](setting-a-security-level-for-access-checks.md) estiver definido para **executar verificações de acesso no nível do processo e do componente**.

**Para habilitar ou desabilitar verificações de acesso no nível do componente**

1.  Na árvore de console da ferramenta administrativa serviços de componentes, localize o aplicativo COM+ que contém o componente para o qual você deseja desabilitar (ou habilitar) as verificações de função. Expanda a exibição na árvore para exibir os componentes na pasta **componentes** .

2.  Clique com o botão direito do mouse no componente para o qual você deseja habilitar as verificações de função e clique em **Propriedades**.

3.  Na caixa de diálogo Propriedades do componente, clique na guia **segurança** .

4.  Selecione **impor verificações de acesso no nível do componente** para impor verificações de nível de componente.

5.  Clique em **OK**.

A nova configuração entrará em vigor na próxima vez em que o aplicativo for iniciado.

> [!Note]  
> A partir do Windows Server 2003, as verificações de acesso no nível de componente são desabilitadas por padrão durante a criação de um aplicativo COM+. As verificações de acesso são habilitadas por padrão no nível do aplicativo e desabilitadas por padrão no nível do componente. Anteriormente, as verificações de acesso foram desabilitadas por padrão no nível do aplicativo e habilitadas por padrão no nível do componente.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Atribuindo funções a componentes, interfaces ou métodos](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[Configurando a segurança do Role-Based](configuring-role-based-security.md)
</dt> <dt>

[Definindo funções para um aplicativo](defining-roles-for-an-application.md)
</dt> <dt>

[Habilitando verificações de acesso para um aplicativo](enabling-access-checks-for-an-application.md)
</dt> <dt>

[Configurando um nível de segurança para verificações de acesso](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



