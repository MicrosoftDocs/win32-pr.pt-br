---
description: O seguinte fornece algumas instâncias comuns de instruções condicionais. Para obter mais informações, consulte Sintaxe de instrução condicional.
ms.assetid: 8b6bae7a-20ae-494c-bd96-66bd537c8630
title: Exemplos de sintaxe de instrução condicional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca91a2b3e89160fad19ad5d9b1c6a3d33929e5d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921419"
---
# <a name="examples-of-conditional-statement-syntax"></a>Exemplos de sintaxe de instrução condicional

O seguinte fornece algumas instâncias comuns de instruções condicionais. Para obter mais informações, consulte [sintaxe de instrução condicional](conditional-statement-syntax.md).

## <a name="run-action-on-removal"></a>Executar ação na remoção.

Para obter informações, consulte [ações de condicionamento a serem executadas durante a remoção](conditioning-actions-to-run-during-removal.md).

## <a name="run-action-only-if-the-product-has-not-been-installed"></a>Execute a ação somente se o produto não tiver sido instalado.

``` syntax
NOT Installed
```

## <a name="run-action-only-if-the-product-will-be-installed-local-do-not-run-action-on-a-reinstallation"></a>Execute a ação somente se o produto for instalado localmente. Não execute a ação em uma reinstalação.

``` syntax
(&FeatureName=3) AND NOT(!FeatureName=3)
```

O termo "&FeatureName = 3" significa que a ação é instalar o recurso local. O termo "não (! FeatureName = 3) "significa que o recurso não está instalado localmente.

## <a name="run-action-only-if-the-feature-will-be-uninstalled"></a>Executar ação somente se o recurso for desinstalado.

``` syntax
(&FeatureName=2) AND (!FeatureName=3)
```

Essa condição verifica apenas uma transição do recurso de um estado instalado de local para o estado ausente.

## <a name="run-action-only-if-the-component-was-installed-local-but-is-transitioning-out-of-state"></a>Executar ação somente se o componente tiver sido instalado localmente, mas estiver em transição fora do estado.

``` syntax
(?ComponentName=3) AND ($ComponentName=2 OR $ComponentName=4)
```

O termo "? ComponetName = 3 "significa que o componente está instalado localmente. O termo "$ComponentName = 2" significa que o estado de ação no componente está ausente. O termo "$ComponentName = 4" significa que o estado de ação no componente é executado a partir da origem. Observe que um estado de ação de advertise não é válido para um componente.

## <a name="run-action-only-on-the-reinstallation-of-a-component"></a>Execute a ação somente na reinstalação de um componente.

``` syntax
?ComponentName=$ComponentName
```

## <a name="run-action-only-when-a-particular-patch-is-applied"></a>Executar ação somente quando um patch específico for aplicado.

``` syntax
PATCH AND PATCH >< MEDIASRCPROPNAME
```

Para obter mais informações, consulte a seção comentários na página de propriedades [**patch**](patch.md) .

 

 



