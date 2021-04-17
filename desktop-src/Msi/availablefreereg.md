---
description: A propriedade AVAILABLEFREEREG especifica, em quilobytes, o total de espaço livre disponível no registro depois de chamar a ação AllocateRegistrySpace. O valor máximo da propriedade AVAILABLEFREEREG é de 2 milhões quilobytes. Essa propriedade é definida somente no Windows 2000.
ms.assetid: 95afc397-2f28-4ab9-8d95-d071c2f1f498
title: Propriedade AVAILABLEFREEREG
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 517073748195c47ee27b68adbe70d6c69f3f585b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748990"
---
# <a name="availablefreereg-property"></a>Propriedade AVAILABLEFREEREG

A propriedade **AVAILABLEFREEREG** especifica, em quilobytes, o total de espaço livre disponível no registro depois de chamar a [ação AllocateRegistrySpace](allocateregistryspace-action.md).

O valor máximo da propriedade **AVAILABLEFREEREG** é de 2 milhões quilobytes.

Essa propriedade é definida somente no Windows 2000.

## <a name="remarks"></a>Comentários

A propriedade **AVAILABLEFREEREG** deve ser definida com um valor grande o suficiente para garantir espaço suficiente no registro para todas as informações de Registro adicionadas pela instalação. O valor mínimo necessário para garantir espaço suficiente depende de onde a [ação AllocateRegistrySpace](allocateregistryspace-action.md) está localizada na sequência de ações, pois o instalador aumenta automaticamente o espaço conforme necessário ao registrar informações nas tabelas [registro](registry-table.md), [classe](class-table.md), [selfreg](selfreg-table.md), [extensão](extension-table.md), [MIME](mime-table.md)e [verbo](verb-table.md) . O instalador não aumenta o espaço total do registro para o valor especificado por **AVAILABLEFREEREG** até chegar a AllocateRegistrySpace na sequência de ação.

Se AllocateRegistrySpace for uma das primeiras ações na sequência de ação, **AVAILABLEFREEREG** deverá ser definido como o espaço total exigido pelas informações de registro na tabela do registro, na tabela de classes, na tabela de typelib, na tabela selfreg, na tabela de extensão, na tabela de MIME, na tabela de verbos, no registro de [ações personalizadas](custom-actions.md) , no auto-registro e em qualquer outra informação de registro gravada durante a instalação O valor de **AVAILABLEFREEREG** é a quantidade total de informações adicionadas pela instalação e garante espaço suficiente em todos os casos. Esse também é o caso mais comum.

Se a ação AllocateRegistrySpace puder ser criada na sequência de ação após todas as [ações padrão](standard-actions.md) que gravam dados de registro, como [WriteRegistryValues](writeregistryvalues-action.md) e [RegisterClassInfo](registerclassinfo-action.md), o valor de **AVAILABLEFREEREG** precisará ser definido apenas como o espaço necessário para registrar ações personalizadas, registrar bibliotecas de tipos e quaisquer outras informações ainda não registradas por meio das tabelas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




