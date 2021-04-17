---
description: No Windows 2000 e sistemas operacionais posteriores, o instalador definirá a propriedade MsiNTSuiteSmallBusinessRestricted como 1 se o Microsoft Small Business Server estiver instalado com a licença de cliente restritiva em vigor.
ms.assetid: a7100df4-6fe4-4159-ba94-9b5bd1803107
title: Propriedade MsiNTSuiteSmallBusinessRestricted
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71d85fa7fe83c0c8c7cd40788453d1078e7a6b94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747535"
---
# <a name="msintsuitesmallbusinessrestricted-property"></a>Propriedade MsiNTSuiteSmallBusinessRestricted

No Windows 2000 e sistemas operacionais posteriores, o instalador definirá a propriedade **MsiNTSuiteSmallBusinessRestricted** como 1 se o Microsoft Small Business Server estiver instalado com a licença de cliente restritiva em vigor. O instalador definirá essa propriedade como 1 somente se o \_ sinalizador restrito do SMALLBUSINESS do pacote de ver \_ \_ estiver definido na estrutura [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) . Caso contrário, o instalador não definirá essa propriedade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 
