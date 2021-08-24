---
description: No WMI, uma classe é um objeto que descreve algum aspecto de uma empresa, como um tipo especial de unidade de disco.
ms.assetid: 06b75910-f126-48b6-8e43-4a9ed4661732
ms.tgt_platform: multiple
title: Criando uma classe WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec2db62f1f0d14035f7bcc3fd74f8bbbfbacf08cb0dbf139b06c9870b7039e19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612556"
---
# <a name="creating-a-wmi-class"></a>Criando uma classe WMI

No WMI, uma classe é um objeto que descreve algum aspecto de uma empresa, como um tipo especial de unidade de disco. Depois de criar uma definição de classe, grave seu provedor DLL para fornecer instâncias da classe, dados de propriedade e métodos de execução definidos para a classe. Scripts e aplicativos podem então obter dados ou controlar o dispositivo. Para obter mais informações, consulte [desenvolvendo um provedor WMI](developing-a-wmi-provider.md).

> [!Note]  
> Para garantir que todas as suas definições de classe WMI para objetos gerenciados sejam restauradas no [*repositório do WMI*](gloss-w.md) se o WMI tiver uma falha e for reiniciado, use a instrução de pré-processador de instrução de [**\# AutoRecuperação pragma**](pragma-autorecover.md) em seu arquivo MOF.

 

## <a name="base-class"></a>Classe base

Uma classe base representa algum conceito geral. Por exemplo, a classe [**CIM \_ CDROMDrive**](/windows/desktop/CIMWin32Prov/cim-cdromdrive) representa todos os tipos de unidades de CD-ROM no WMI e contém propriedades gerais que descrevem todos os tipos de unidades de CD-ROM. Para obter mais informações, consulte [criando uma classe base](creating-a-base-class.md).

Uma classe derivada herda propriedades e métodos de outra classe. Uma classe derivada geralmente representa um caso específico de uma classe base. por exemplo, a classe [**Win32 \_ CDROMDrive**](/windows/desktop/CIMWin32Prov/win32-cdromdrive) representa uma unidade de CD-ROM em um sistema Windows. A classe **Win32 \_ CDROMDrive** baseia-se em e herda muitas propriedades de [**CIM \_ CDROMDrive**](/windows/desktop/CIMWin32Prov/cim-cdromdrive). No entanto, o **Win32 \_ CDROMDrive**, como outras classes derivadas, pode ter propriedades adicionais que tornam a classe derivada exclusiva. Para obter mais informações, consulte [criando uma classe derivada](creating-a-derived-class.md).

## <a name="properties-and-methods"></a>Propriedades e métodos

Criar uma classe significa definir as propriedades que descrevem essa classe. Você também pode definir métodos que manipulam o objeto representado pela classe.

Geralmente, uma propriedade representa um aspecto do objeto, como um número de série para um dispositivo ou um tamanho em bytes para um processo, enquanto um método representa uma ação que altera o estado ou o comportamento do dispositivo ou da entidade lógica.

Cada classe deve ter pelo menos uma propriedade de chave. Embora uma classe possa ter várias chaves, você não pode criar uma instância de uma classe com mais de 256 chaves.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando classes formato MOF (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 
