---
description: O exemplo a seguir fornece algumas instâncias comuns de instruções condicionais. Para obter mais informações, consulte Sintaxe de instrução condicional.
ms.assetid: 8b6bae7a-20ae-494c-bd96-66bd537c8630
title: Exemplos de sintaxe de instrução condicional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88445e1e4b371669c43b47d1ca54e9fd677c5414985ade3908b95e00717de887
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811026"
---
# <a name="examples-of-conditional-statement-syntax"></a>Exemplos de sintaxe de instrução condicional

O exemplo a seguir fornece algumas instâncias comuns de instruções condicionais. Para obter mais informações, consulte [Sintaxe de instrução condicional](conditional-statement-syntax.md).

## <a name="run-action-on-removal"></a>Execute a ação na remoção.

Para obter informações, consulte [Ações de condicionação a executar durante a remoção.](conditioning-actions-to-run-during-removal.md)

## <a name="run-action-only-if-the-product-has-not-been-installed"></a>Execute a ação somente se o produto não tiver sido instalado.

``` syntax
NOT Installed
```

## <a name="run-action-only-if-the-product-will-be-installed-local-do-not-run-action-on-a-reinstallation"></a>Execute a ação somente se o produto for instalado localmente. Não execute a ação em uma reinstalação.

``` syntax
(&FeatureName=3) AND NOT(!FeatureName=3)
```

O termo "&FeatureName=3" significa que a ação é instalar o recurso local. O termo "NOT(! FeatureName=3)" significa que o recurso não está instalado localmente.

## <a name="run-action-only-if-the-feature-will-be-uninstalled"></a>Execute a ação somente se o recurso for desinstalado.

``` syntax
(&FeatureName=2) AND (!FeatureName=3)
```

Essa condição verifica apenas uma transição do recurso de um estado instalado de local para o estado ausente.

## <a name="run-action-only-if-the-component-was-installed-local-but-is-transitioning-out-of-state"></a>Execute a ação somente se o componente tiver sido instalado localmente, mas estiver em transição para fora do estado.

``` syntax
(?ComponentName=3) AND ($ComponentName=2 OR $ComponentName=4)
```

O termo "? ComponetName=3" significa que o componente está instalado localmente. O termo "$ComponentName=2" significa que o estado da ação no componente é Absent. O termo "$ComponentName=4" significa que o estado da ação no componente é executado da origem. Observe que um estado de ação de anúncio não é válido para um componente.

## <a name="run-action-only-on-the-reinstallation-of-a-component"></a>Execute a ação somente na reinstalação de um componente.

``` syntax
?ComponentName=$ComponentName
```

## <a name="run-action-only-when-a-particular-patch-is-applied"></a>Execute a ação somente quando um patch específico for aplicado.

``` syntax
PATCH AND PATCH >< MEDIASRCPROPNAME
```

Para obter mais informações, consulte a seção Comentários na página [**de propriedades PATCH.**](patch.md)

 

 



