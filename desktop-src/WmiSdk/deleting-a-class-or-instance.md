---
description: Depois de terminar com uma classe ou uma instância, talvez você queira excluir essa classe ou instância do WMI.
ms.assetid: 8d4bf548-a332-4058-92d0-d613bbeaa408
ms.tgt_platform: multiple
title: Excluindo uma classe ou instância
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42a46a52400623e31df3e051a0b587f49326733b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165333"
---
# <a name="deleting-a-class-or-instance"></a>Excluindo uma classe ou instância

Depois de terminar com uma classe ou uma instância, talvez você queira excluir essa classe ou instância do WMI. Assim como outras tecnologias orientadas a objeto, você pode excluir objetos de classe ou instância para limpar o namespace WMI e para retornar recursos do sistema. No entanto, muitas classes e instâncias no WMI são persistentes e são usadas por uma variedade de aplicativos a qualquer momento, portanto, você deve ter cuidado ao excluir uma classe ou instância WMI: seu aplicativo ou outro aplicativo provavelmente precisará da classe ou instância em uma data posterior.

Excluir uma classe ou uma instância é um procedimento simples. No entanto, devido à natureza permanente de uma classe, provavelmente não será necessário excluir uma classe com frequência. Por exemplo, é improvável que você exclua a classe [**Win32 \_ DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive) , pois é improvável que você não tenha uma unidade de disco em algum lugar em sua empresa. Em vez disso, será mais provável que você exclua uma instância de uma classe. Para obter mais informações, consulte [excluindo uma instância](deleting-an-instance.md).

Embora não seja comum, você pode chegar a um momento em que deseja atualizar uma classe que você criou. Por exemplo, você pode criar uma classe para representar um aplicativo de terceiros. Se a terceira parte tiver atualizado seu software na medida em que sua classe não representou o software mais corretamente, talvez seja necessário excluir sua classe original. Para obter mais informações, consulte [excluindo uma classe](deleting-a-class.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando classes formato MOF (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 
