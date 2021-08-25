---
title: WINBIO_DB constantes (tipos \_ Winbio.h)
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
ms.openlocfilehash: 0a9d8392fd38e9d53588002c8aeab688ffc8b76efced83819318d9c6b6c2b721
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867976"
---
# <a name="winbio_db-constants"></a>Constantes de BD WINBIO \_

As constantes a seguir podem ser usadas ao chamar [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) para especificar o banco de dados a ser usado para um pool de sistema.



| Constante                                                                                                                                                                         | Descrição                                                                                                                                                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DB_DEFAULT"></span><span id="winbio_db_default"></span><dl> <dt>**WINBIO \_ DB \_ DEFAULT**</dt> </dl>       | Cada unidade biométrica no pool de sensor usa o banco de dados padrão especificado na configuração de unidade biométrica padrão.<br/>                                                                   |
| <span id="WINBIO_DB_BOOTSTRAP"></span><span id="winbio_db_bootstrap"></span><dl> <dt>**INICIALIZAÇÃO \_ DE BD WINBIO \_**</dt> </dl> | Pode ser usado para cenários antes de iniciar Windows. Normalmente, o banco de dados faz parte do chip do sensor ou faz parte do BIOS e só pode ser usado para registro e exclusão de modelo.<br/> |
| <span id="WINBIO_DB_ONCHIP"></span><span id="winbio_db_onchip"></span><dl> <dt>**WINBIO \_ DB \_ ONCHIP**</dt> </dl>          | O banco de dados reside no chip do sensor.<br/>                                                                                                                                                  |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                                    |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                                                       |
| Cabeçalho<br/>                   | <dl> <dt>Winbio \_ types.h (inclua Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes de aplicativo cliente](client-application-constants.md)
</dt> </dl>

 

 





