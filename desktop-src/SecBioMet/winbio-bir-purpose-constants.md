---
title: Constantes de WINBIO_BIR_PURPOSE (WinBio \_ Types. h)
description: Especifique a finalidade para a qual o registro de informações biométricas (BIR) é pretendido ou para o qual ele é adequado.
ms.assetid: AAFD3203-4D3D-43B5-A833-1258E1E281D3
topic_type:
- apiref
api_name:
- WINBIO_NO_PURPOSE_AVAILABLE
- WINBIO_PURPOSE_VERIFY
- WINBIO_PURPOSE_IDENTIFY
- WINBIO_PURPOSE_ENROLL
- WINBIO_PURPOSE_ENROLL_FOR_VERIFICATION
- WINBIO_PURPOSE_ENROLL_FOR_IDENTIFICATION
- WINBIO_PURPOSE_AUDIT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5a662a5ae045d3afc631f93cdf296508dabccf9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918505"
---
# <a name="winbio_bir_purpose-constants"></a>Constantes de finalidade de \_ Bir WINBIO \_

Os sinalizadores a seguir são usados pelo membro de **finalidade** da estrutura de [**\_ \_ cabeçalho WINBIO Bir**](winbio-bir-header.md) para especificar a finalidade para a qual o Bir (registro de informações biométricas) é pretendido ou para o qual ele é adequado.



| Constante                                                                                                                                                                                                                                          | Descrição                                                                                                                                                                                                                                                                                                                                 |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_NO_PURPOSE_AVAILABLE"></span><span id="winbio_no_purpose_available"></span><dl> <dt>**WINBIO \_ nenhuma \_ finalidade \_ disponível**</dt> </dl>                                         | Nenhuma finalidade foi especificada.<br/>                                                                                                                                                                                                                                                                                                         |
| <span id="WINBIO_PURPOSE_VERIFY"></span><span id="winbio_purpose_verify"></span><dl> <dt>**\_verificação de finalidade do WINBIO \_**</dt> </dl>                                                            | Verifique a identidade de um usuário.<br/>                                                                                                                                                                                                                                                                                                   |
| <span id="WINBIO_PURPOSE_IDENTIFY"></span><span id="winbio_purpose_identify"></span><dl> <dt>**\_identificação de finalidade do WINBIO \_**</dt> </dl>                                                      | Identificar um usuário.<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="WINBIO_PURPOSE_ENROLL"></span><span id="winbio_purpose_enroll"></span><dl> <dt>**\_registro de finalidade do WINBIO \_**</dt> </dl>                                                            | Registrar um usuário.<br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="WINBIO_PURPOSE_ENROLL_FOR_VERIFICATION"></span><span id="winbio_purpose_enroll_for_verification"></span><dl> <dt>**\_ \_ registro de finalidade \_ do WINBIO para \_ verificação**</dt> </dl>       | Capture um exemplo biométrico e determine se o exemplo corresponde à identidade de usuário especificada.<br/>                                                                                                                                                                                                                          |
| <span id="WINBIO_PURPOSE_ENROLL_FOR_IDENTIFICATION"></span><span id="winbio_purpose_enroll_for_identification"></span><dl> <dt>**\_ \_ registro de finalidade \_ do WINBIO para \_ identificação**</dt> </dl> | Capture um exemplo biométrico e determine se ele corresponde a um modelo biométrico existente.<br/>                                                                                                                                                                                                                                      |
| <span id="WINBIO_PURPOSE_AUDIT"></span><span id="winbio_purpose_audit"></span><dl> <dt>**\_auditoria de finalidade do WINBIO \_**</dt> </dl>                                                               | Informações extras que podem ser usadas para registro em log ou para exibição. Esse valor é ignorado na entrada por todas as funções. Na saída, ela só estará disponível se houver suporte da unidade biométrica e você especificar o **\_ sinalizador de dados WINBIO \_ \_ RAW** no parâmetro *flags* da função [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample) .<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                                    |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                                       |
| parâmetro<br/>                   | <dl> <dt>WinBio \_ Types. h (inclui WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes de aplicativo cliente](client-application-constants.md)
</dt> <dt>

[**\_cabeçalho WINBIO Bir \_**](winbio-bir-header.md)
</dt> </dl>

 

 





