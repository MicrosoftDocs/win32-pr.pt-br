---
description: A propriedade AVAILABLEFREEREG especifica em quilobytes o espaço livre total disponível no Registro depois de chamar a ação AllocateRegistrySpace. O valor máximo da propriedade AVAILABLEFREEREG é 2000000 quilobytes. Essa propriedade é definida somente no Windows 2000.
ms.assetid: 95afc397-2f28-4ab9-8d95-d071c2f1f498
title: Propriedade AVAILABLEFREEREG
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b45508494f9ba87ec8261b38ea18f83d0b3ad9796f7390b70349211cbf244df3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650066"
---
# <a name="availablefreereg-property"></a>Propriedade AVAILABLEFREEREG

A **propriedade AVAILABLEFREEREG** especifica em quilobytes o espaço livre total disponível no Registro depois de chamar a ação [AllocateRegistrySpace](allocateregistryspace-action.md).

O valor máximo da **propriedade AVAILABLEFREEREG** é 2000000 quilobytes.

Essa propriedade é definida somente no Windows 2000.

## <a name="remarks"></a>Comentários

A **propriedade AVAILABLEFREEREG** deve ser definida como um valor grande o suficiente para garantir espaço suficiente no Registro para todas as informações de registro adicionadas pela instalação. O valor mínimo necessário para garantir espaço suficiente depende de onde a ação [AllocateRegistrySpace](allocateregistryspace-action.md) está localizada na sequência de ação, pois o instalador aumenta automaticamente o espaço conforme necessário ao registrar informações nas tabelas [Registry](registry-table.md), [Class](class-table.md), [SelfReg](selfreg-table.md), [Extension](extension-table.md), [MIME](mime-table.md)e [Verb.](verb-table.md) O instalador não aumenta o espaço total do Registro para o valor especificado por **AVAILABLEFREEREG** até alcançar AllocateRegistrySpace na sequência de ação.

Se AllocateRegistrySpace for uma das primeiras ações na sequência de ação, **AVAILABLEFREEREG** deverá ser definido como o espaço total exigido pelas informações de registro na tabela do Registro, tabela Classe, tabela TypeLib, tabela SelfReg, Tabela de extensão, tabela MIME, tabela [Verb,](custom-actions.md) registro de ações personalizadas, registro de autoregisão e quaisquer outras informações do Registro escritas durante a instalação. O valor de **AVAILABLEFREEREG** é a quantidade total de informações adicionadas pela instalação e garante espaço suficiente em todos os casos. Esse também é o caso mais comum.

Se a ação AllocateRegistrySpace puder ser escrita [](standard-actions.md) na sequência de ação após todas as ações padrão que escrevem dados de registro, como [WriteRegistryValues](writeregistryvalues-action.md) e [RegisterClassInfo](registerclassinfo-action.md), o valor **de AVAILABLEFREEREG** só precisará ser definido para o espaço necessário para registrar ações personalizadas, registrar bibliotecas de tipo e quaisquer outras informações ainda não registradas por meio das tabelas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP. Consulte o [Windows instalador Run-Time para](windows-installer-portal.md) obter informações sobre o Windows service pack mínimo exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




