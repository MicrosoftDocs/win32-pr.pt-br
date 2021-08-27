---
description: em Windows 2000 e sistemas operacionais posteriores, o instalador definirá a propriedade MsiNTSuiteWebServer como 1 se o instalador estiver em execução em uma web edition do Windows Server 2003.
ms.assetid: de462ba2-4654-4f47-9dd7-3bc9c6f0af0e
title: Propriedade MsiNTSuiteWebServer
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60c920dc97733a6a8bc134f2ac0c76d449afd6a5ce39e5f8e0555d30daa78952
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129216"
---
# <a name="msintsuitewebserver-property"></a>Propriedade MsiNTSuiteWebServer

em Windows 2000 e sistemas operacionais posteriores, o instalador definirá a propriedade **MsiNTSuiteWebServer** como 1 se o instalador estiver em execução em uma web edition do Windows Server 2003. O instalador definirá essa propriedade como 1 somente se o \_ sinalizador de lâmina do pacote de ver \_ estiver definido na estrutura [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) . Caso contrário, o instalador não definirá essa propriedade.

## <a name="remarks"></a>Comentários

essa propriedade está disponível somente com a versão 2003 do instalador do Windows Server.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP. consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o service pack mínimo Windows exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[sem suporte no Windows Installer 2,0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 
