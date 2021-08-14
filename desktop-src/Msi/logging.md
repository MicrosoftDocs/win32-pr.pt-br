---
description: Essa política de sistema por computador será usada somente se o registro em log não tiver sido habilitado pelo &\# 0034;/L&0034; opção de linha de comando ou \# por MsiEnableLog.
ms.assetid: d8649808-5dc3-4496-8c2f-da9b1512b5aa
title: Registro em log (Windows Instalador)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49993419b03e3c092fdf4d2b6d9d118ca4dc2d3d641c82c4fc829cbfd6b68c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945631"
---
# <a name="logging-windows-installer"></a>Registro em log (Windows Instalador)

Essa política de sistema por [computador](system-policy.md) será usada somente se o registro em log não tiver sido habilitado pela opção de linha de comando "/L" ou [**por MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga). Se a política for definida nesse caso, o instalador criará um arquivo de log em %temp% com o nome aleatório: MSI \* . Log. Especifique o modo de registro em log definindo o valor da política como uma cadeia de caracteres. Use os mesmos caracteres para especificar a política de modo de registro em log, conforme usado pela opção de linha de comando ["/L".](command-line-options.md) Observe que você não pode usar "+" e \* "" para a política.

O modo de registro em log pode ser definido usando a política, uma opção de linha de comando ou programaticamente. Para obter mais informações sobre todos os métodos disponíveis para definir o modo de registro em log, consulte Registro em log [normal](normal-logging.md) na seção registro em log do [Windows Instalador.](windows-installer-logging.md)

Você pode impedir que informações confidenciais, por exemplo, senhas, possam ser inseridas no arquivo de log e se tornou visíveis. Para obter mais informações, [consulte Impedindo que informações confidenciais são escritas no arquivo de log](preventing-confidential-information-from-being-written-into-the-log-file.md)

## <a name="registry-key"></a>Chave do Registro

De definir o valor chamado Registro em log na chave do Registro a seguir.

**HKEY \_ Instalador \_ do** Microsoft machine \\ **software** \\ **policies** \\  \\ **microsoft Windows** \\ 

## <a name="data-type"></a>Tipo de Dados

**REG \_ SZ**

 

 



