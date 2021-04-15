---
title: Constantes de WINBIO_FLAG (WinBio \_ Types. h)
description: Especifique a configuração da unidade biométrica e as características de acesso para a nova sessão.
ms.assetid: 82b57023-6c27-433d-bf13-f136f501fc60
topic_type:
- apiref
api_name:
- WINBIO_FLAG_DEFAULT
- WINBIO_FLAG_BASIC
- WINBIO_FLAG_ADVANCED
- WINBIO_FLAG_RAW
- WINBIO_FLAG_MAINTENANCE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ed632b5f15cc3d6a7ac6b0c6c70a2b3431b73db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369344"
---
# <a name="winbio_flag-constants"></a>\_Constantes de sinalizador WINBIO

As constantes a seguir podem ser usadas na função [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) para especificar a configuração de unidade biométrica e as características de acesso para a nova sessão.



| Constante                                                                                                                                                                                     | Descrição                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_FLAG_DEFAULT"></span><span id="winbio_flag_default"></span><dl> <dt>**\_padrão de sinalizador WINBIO \_**</dt> </dl>             | Sinalizador de configuração do sensor. As unidades biométricas operam da maneira especificada durante a instalação.<br/>                                                                           |
| <span id="WINBIO_FLAG_BASIC"></span><span id="winbio_flag_basic"></span><dl> <dt>**\_sinalizador WINBIO \_ básico**</dt> </dl>                   | Sinalizador de configuração do sensor. As unidades biométricas operam apenas como dispositivos básicos de captura.<br/>                                                                                         |
| <span id="WINBIO_FLAG_ADVANCED"></span><span id="winbio_flag_advanced"></span><dl> <dt>**\_sinalizador WINBIO \_ avançado**</dt> </dl>          | Sinalizador de configuração do sensor. As unidades biométricas usam recursos internos de processamento e armazenamento.<br/>                                                                              |
| <span id="WINBIO_FLAG_RAW"></span><span id="winbio_flag_raw"></span><dl> <dt>**WINBIO de \_ sinalizador \_ bruto**</dt> </dl>                         | Sinalizador de acesso desejado. O aplicativo cliente captura dados biométricos brutos usando [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample).<br/>                                             |
| <span id="WINBIO_FLAG_MAINTENANCE"></span><span id="winbio_flag_maintenance"></span><dl> <dt>**\_manutenção do sinalizador WINBIO \_**</dt> </dl> | Sinalizador de acesso desejado. O cliente executa operações de controle definidas pelo fornecedor em uma unidade biométrica chamando [**WinBioControlUnitPrivileged**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged).<br/> |



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

 

 





