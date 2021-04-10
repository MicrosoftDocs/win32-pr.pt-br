---
description: Um aplicativo pode usar a função RegSetValueEx para associar um valor e seus dados a uma chave. Para obter uma lista dos tipos de valor com suporte em RegSetValueEx, consulte tipos de valor do registro.
ms.assetid: 75ac826a-f169-400c-b6d6-3e3ec9ebf996
title: Gravando e excluindo dados do registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5185c98f39a37512ec56fb994d5f1c4ba4b61ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296655"
---
# <a name="writing-and-deleting-registry-data"></a>Gravando e excluindo dados do registro

Um aplicativo pode usar a função [**RegSetValueEx**](/windows/desktop/api/Winreg/nf-winreg-regsetvalueexa) para associar um valor e seus dados a uma chave. Para obter uma lista dos tipos de valor com suporte em **RegSetValueEx**, consulte [tipos de valor do registro](registry-value-types.md).

Para excluir um valor de uma chave, um aplicativo pode usar a função [**falha em RegDeleteValue**](/windows/desktop/api/Winreg/nf-winreg-regdeletevaluea) . Para excluir uma chave, ela pode usar a função [**RegDeleteKey**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeya) . Uma chave excluída não é removida até que o último identificador para ela tenha sido fechado. Subchaves e valores não podem ser criados sob uma chave excluída.

Não é possível bloquear uma chave do registro durante uma operação de gravação para sincronizar o acesso aos dados. No entanto, você pode controlar o acesso a uma chave do registro usando atributos de segurança. Para obter mais informações, consulte [segurança da chave do registro e direitos de acesso](registry-key-security-and-access-rights.md).

Mais de uma operação de registro pode ser executada em uma única transação. Para associar uma chave do registro a uma transação, um aplicativo pode usar a função [**RegCreateKeyTransacted**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeytransacteda) ou [**RegOpenKeyTransacted**](/windows/desktop/api/Winreg/nf-winreg-regopenkeytransacteda) . Para obter mais informações sobre transações, consulte [kernel Transaction Manager](/windows/desktop/Ktm/kernel-transaction-manager-portal).

 

 
