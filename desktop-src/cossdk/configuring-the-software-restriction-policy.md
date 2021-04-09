---
description: Configurando a política de restrição de software
ms.assetid: 22c1897a-abb5-4ce9-9d09-21b6aed4f1d8
title: Configurando a política de restrição de software
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 522f216af6957ebd23bc9f17c70f61cab2cabc5c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010265"
---
# <a name="configuring-the-software-restriction-policy"></a>Configurando a política de restrição de software

Quando você define explicitamente os níveis de confiança da diretiva de restrição de software de um aplicativo do COM+, você está substituindo as configurações padrão de todo o grupo. Isso geralmente é necessário para aplicativos de servidor COM+ porque o nível de confiança do todo o grupo é definido como o mesmo para todos os aplicativos de servidor (porque todos eles são executados no mesmo arquivo, dllhost.exe). No entanto, quando você define o nível de confiança da diretiva de restrição de software de um aplicativo de biblioteca COM+, está afetando a configuração de todo o grupo para esse aplicativo. Para obter uma discussão sobre como usar a política de restrição de software no COM+, consulte [usando a política de restrição de software no com+](using-the-software-restriction-policy-in-com-.md).

**Para definir a diretiva de restrição de software**

1.  Clique com o botão direito do mouse no aplicativo COM+ para o qual você está definindo a diretiva de restrição de software e clique em **Propriedades**.

2.  Na caixa de diálogo Propriedades do aplicativo, clique na guia **segurança** .

3.  Em **diretiva de restrição de software**, marque a caixa de seleção **aplicar política de restrição de software** ; Isso permite que você defina o nível de confiança. Desmarcar a caixa de seleção fará com que o COM+ use a configuração em todo o âmbito da diretiva de restrição de software para o aplicativo. Essa caixa de seleção corresponde à propriedade SRPEnabled da coleção de [**aplicativos**](applications.md) .

4.  Na caixa **nível de restrição** , selecione o nível apropriado. Essa caixa suspensa corresponde à propriedade SRPTrustLevel da coleção de [**aplicativos**](applications.md) . Os níveis são os seguintes, ordenados do menos para o mais confiável:

    -   Não **permitido**. O aplicativo não é permitido de usar os privilégios totais do usuário. Os componentes com qualquer nível de confiança podem ser carregados nele.
    -   **Irrestrito**. O aplicativo tem acesso irrestrito aos privilégios do usuário. Somente os componentes com um nível de confiança irrestrito podem ser carregados nele.

5.  Clique em **OK**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando a segurança do Role-Based](configuring-role-based-security.md)
</dt> <dt>

[Habilitando a autenticação para um aplicativo de biblioteca](enabling-authentication-for-a-library-application.md)
</dt> <dt>

[Definindo um nível de autenticação para um aplicativo de servidor](setting-an-authentication-level-for-a-server-application.md)
</dt> <dt>

[Definindo um nível de representação](setting-an-impersonation-level.md)
</dt> </dl>

 

 



