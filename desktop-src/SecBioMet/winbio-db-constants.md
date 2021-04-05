---
title: Constantes de WINBIO_DB (WinBio \_ Types. h)
description: Especifique o banco de dados a ser usado para um pool do sistema.
ms.assetid: 2cffa455-5834-4a35-b8d8-f9d1feddcaa1
topic_type:
- apiref
api_name:
- WINBIO_DB_DEFAULT
- WINBIO_DB_BOOTSTRAP
- WINBIO_DB_ONCHIP
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20503e1dc3cd7b5e47651889dd9c67777614593c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085785"
---
# <a name="winbio_db-constants"></a>Constantes do WINBIO \_ DB

As constantes a seguir podem ser usadas ao chamar [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) para especificar o banco de dados a ser usado para um pool do sistema.



| Constante                                                                                                                                                                         | Descrição                                                                                                                                                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DB_DEFAULT"></span><span id="winbio_db_default"></span><dl> <dt>**padrão do WINBIO \_ DB \_**</dt> </dl>       | Cada unidade biométrica no pool de sensores usa o banco de dados padrão especificado na configuração de unidade biométrica padrão.<br/>                                                                   |
| <span id="WINBIO_DB_BOOTSTRAP"></span><span id="winbio_db_bootstrap"></span><dl> <dt>**inicialização do WINBIO \_ DB \_**</dt> </dl> | Pode ser usado para cenários antes de iniciar o Windows. Normalmente, o banco de dados faz parte do chip do sensor ou faz parte do BIOS e só pode ser usado para registro e exclusão de modelo.<br/> |
| <span id="WINBIO_DB_ONCHIP"></span><span id="winbio_db_onchip"></span><dl> <dt>**WINBIO \_ DB \_ OnChip**</dt> </dl>          | O banco de dados reside no chip do sensor.<br/>                                                                                                                                                  |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                                    |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                                       |
| parâmetro<br/>                   | <dl> <dt>WinBio \_ Types. h (inclui WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes de aplicativo cliente](client-application-constants.md)
</dt> </dl>

 

 





