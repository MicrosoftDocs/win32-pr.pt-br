---
title: '\_Constantes de erro de certificado EAP (Eaphosterror. h)'
description: Defina erros relacionados a certificados comuns a todas as tecnologias de API do EAPHost.
ms.assetid: 12f626e1-520a-4aba-954b-769c3062a38c
topic_type:
- apiref
api_name:
- _EAP_CERT_FIRST
- _EAP_CERT_LAST
- _EAP_CERT_NOT_FOUND
- _EAP_CERT_INVALID
- _EAP_CERT_EXPIRED
- _EAP_CERT_REVOKED
- _EAP_CERT_OTHER_ERROR
- _EAP_CERT_REJECTED
- _EAP_CERT_NAME_REQUIRED
- _EAP_GENERAL_FIRST
- _EAP_GENERAL_LAST
api_location:
- eaphosterror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0543636f36d823b5557ad2f5a5f7cb000d93259a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499287"
---
# <a name="eap_cert-error-constants"></a>\_Constantes de erro de certificado EAP

Essas constantes definem erros relacionados a certificados comuns a todas as tecnologias de API do EAPHost.

<dl> <dt>

<span id="_EAP_CERT_FIRST"></span><span id="_eap_cert_first"></span>**\_\_certificado EAP \_ primeiro**
</dt> <dd> <dl> <dt>

0x0
</dt> <dt>



Define o limite dos relatórios de erros; ocorrerá qualquer erro de certificado entre o certificado **\_ EAP \_ \_ primeiro** e o **\_ \_ certificado EAP \_ por último**.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_LAST"></span><span id="_eap_cert_last"></span>**\_\_certificado EAP \_ último**
</dt> <dd> <dl> <dt>

0xF
</dt> <dt>



Define o limite dos relatórios de erros; ocorrerá qualquer erro de certificado entre o certificado **\_ EAP \_ \_ primeiro** e o **\_ \_ certificado EAP \_ por último**.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_NOT_FOUND"></span><span id="_eap_cert_not_found"></span>**\_\_certificado EAP \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

0x1
</dt> <dt>



Nenhum certificado de usuário foi encontrado.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_INVALID"></span><span id="_eap_cert_invalid"></span>**\_\_certificado EAP \_ inválido**
</dt> <dd> <dl> <dt>

0x2
</dt> <dt>



O certificado de usuário é inválido.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_EXPIRED"></span><span id="_eap_cert_expired"></span>**\_\_certificado EAP \_ expirado**
</dt> <dd> <dl> <dt>

0x3
</dt> <dt>



O certificado de usuário expirou.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_REVOKED"></span><span id="_eap_cert_revoked"></span>**\_\_certificado EAP \_ revogado**
</dt> <dd> <dl> <dt>

0x4
</dt> <dt>



O certificado de usuário foi revogado.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_OTHER_ERROR"></span><span id="_eap_cert_other_error"></span>**\_\_ \_ outro erro de certificado EAP \_**
</dt> <dd> <dl> <dt>

0x5
</dt> <dt>



Há um erro desconhecido relacionado ao certificado.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_REJECTED"></span><span id="_eap_cert_rejected"></span>**\_\_certificado EAP \_ rejeitado**
</dt> <dd> <dl> <dt>

0x6
</dt> <dt>



O certificado de usuário foi rejeitado.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_NAME_REQUIRED"></span><span id="_eap_cert_name_required"></span>**\_\_nome de certificado EAP \_ \_ necessário**
</dt> <dd> <dl> <dt>

0x7
</dt> <dt>



O certificado de usuário requer um nome.


</dt> </dl> </dd> <dt>

<span id="_EAP_GENERAL_FIRST"></span><span id="_eap_general_first"></span>**\_EAP \_ geral \_ primeiro**
</dt> <dd> <dl> <dt>

0x10
</dt> <dt>



Define o limite dos relatórios de erros; qualquer erro geral de EAP ocorrerá entre o **\_ EAP \_ geral \_ primeiro** e o **\_ EAP \_ geral, \_ por fim**.


</dt> </dl> </dd> <dt>

<span id="_EAP_GENERAL_LAST"></span><span id="_eap_general_last"></span>**\_EAP \_ geral \_ último**
</dt> <dd> <dl> <dt>

0x3F
</dt> <dt>



Define o limite dos relatórios de erros; qualquer erro geral de EAP ocorrerá entre o **\_ EAP \_ geral \_ primeiro** e o **\_ EAP \_ geral, \_ por fim**.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                      |
| parâmetro<br/>                   | <dl> <dt>Eaphosterror. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes do EAPHost comuns](common-eap-host-error-constants.md)
</dt> </dl>

 

 





