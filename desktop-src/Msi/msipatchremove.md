---
description: A propriedade MSIPATCHREMOVE especifica a lista de patches a serem removidos durante uma instalação.
ms.assetid: 76f8daa9-d32c-4845-85bc-52b728f53d1f
title: Propriedade MSIPATCHREMOVE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1259e42bebdbf44473fb92c666cdb764580c2f54321e7f14d0293b1fa9928103
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944504"
---
# <a name="msipatchremove-property"></a>Propriedade MSIPATCHREMOVE

A propriedade **MSIPATCHREMOVE** especifica a lista de patches a serem removidos durante uma instalação. Os patches individuais na lista são separados por ponto e vírgula e podem ser representados pelo GUID de código de patch ou pelo caminho completo para o patch. A função [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) e o método [**RemovePatches**](installer-removepatches.md) do objeto [instalador](installer-object.md) definem a propriedade **MSIPATCHREMOVE** .

A propriedade **MSIPATCHREMOVE** pode ser definida na linha de comando da seguinte maneira para remover um patch.

**msiexec/i A: \\Example.msi MSIPATCHREMOVE = c: \\ patches \\ qfe1. msp; { 0BBB87F1-3186-409C-8CDD-C88AA2A4A7E0}; {A86B443B-E3BF-4009-ADED-F716FC735858}/QB**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador 3,0 ou posterior no Windows Server 2003 ou Windows XP. consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o service pack mínimo Windows exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[sem suporte no Windows Installer 2,0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




