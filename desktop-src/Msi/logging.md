---
description: Essa política de sistema por computador será usada somente se o log não tiver sido habilitado pela \# opção de linha de comando &0034;/l&\# 0034; ou por MsiEnableLog.
ms.assetid: d8649808-5dc3-4496-8c2f-da9b1512b5aa
title: Registro em log (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a461051022791e414fe7e211e4dde33c7e83101b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662193"
---
# <a name="logging-windows-installer"></a>Registro em log (Windows Installer)

Essa [política do sistema](system-policy.md) por máquina será usada somente se o registro em log não tiver sido habilitado pela opção de linha de comando "/l" ou por [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga). Se a política for definida nesse caso, o instalador criará um arquivo de log em% temp% com o nome aleatório: MSI \* . Façam. Especifique o modo de log definindo o valor da política como uma cadeia de caracteres. Use os mesmos caracteres para especificar a política do modo de log, conforme usado pela [opção de linha de comando](command-line-options.md)"/l". Observe que você não pode usar "+" e " \* " para a política.

O modo de log pode ser definido usando a política, uma opção de linha de comando ou programaticamente. Para obter mais informações sobre todos os métodos que estão disponíveis para definir o modo de log, consulte [log normal](normal-logging.md) na seção [log de Windows Installer](windows-installer-logging.md) .

Você pode impedir que informações confidenciais, por exemplo, senhas, sejam inseridas no arquivo de log e fiquem visíveis. Para obter mais informações, consulte [impedindo que informações confidenciais sejam gravadas no arquivo de log](preventing-confidential-information-from-being-written-into-the-log-file.md)

## <a name="registry-key"></a>Chave do Registro

Defina o valor chamado Logging na seguinte chave do registro.

**HKEY \_ \_** Políticas de \\ **software** do computador local \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de Dados

**REG \_ sz**

 

 



