---
title: Constantes de identidade (AppModel.h)
description: Especifica o comprimento das cadeias de caracteres para os campos de identidade do pacote.
ms.assetid: C4F81822-B502-4360-AEA4-829F1AB926BF
topic_type:
- apiref
api_name:
- APPLICATION_USER_MODEL_ID_MAX_LENGTH
- APPLICATION_USER_MODEL_ID_MIN_LENGTH
- PACKAGE_ARCHITECTURE_MAX_LENGTH
- PACKAGE_ARCHITECTURE_MIN_LENGTH
- PACKAGE_FAMILY_NAME_MAX_LENGTH
- PACKAGE_FAMILY_NAME_MIN_LENGTH
- PACKAGE_FULL_NAME_MAX_LENGTH
- PACKAGE_FULL_NAME_MIN_LENGTH
- PACKAGE_NAME_MAX_LENGTH
- PACKAGE_NAME_MIN_LENGTH
- PACKAGE_PUBLISHERID_MAX_LENGTH
- PACKAGE_PUBLISHERID_MIN_LENGTH
- PACKAGE_PUBLISHER_MAX_LENGTH
- PACKAGE_PUBLISHER_MIN_LENGTH
- PACKAGE_RELATIVE_APPLICATION_ID_MAX_LENGTH
- PACKAGE_RELATIVE_APPLICATION_ID_MIN_LENGTH
- PACKAGE_RESOURCEID_MAX_LENGTH
- PACKAGE_RESOURCEID_MIN_LENGTH
- PACKAGE_VERSION_MAX_LENGTH
- PACKAGE_VERSION_MIN_LENGTH
api_location:
- AppModel.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4590e62397ac069cb0fc9661f615288c2d8df36ba41304fff71e4ef0293f9f3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118552208"
---
# <a name="identity-constants"></a>Constantes de identidade

Especifica o comprimento das cadeias de caracteres para os campos de identidade do pacote. O comprimento é medido em caracteres e pode ou não incluir espaço para o terminador NULL.

> [!Note]  
> Constantes no formato: COMPRIMENTO DA ID DO MODELO DE USUÁRIO DO APLICATIVO e TAMANHO DA **\_ \* \_** **\_ \_ \_ \_ \* \_ ID** DO APLICATIVO RELATIVO DO PACOTE incluem espaço para um terminador NULL, mas constantes no formato: TAMANHO DO PACOTE não incluem espaço para um terminador NULL. **\_ \_ \_ \_ \* \_**

 



| Constante/valor                                                                                                                                                                                                                                                                                                   | Descrição                                                                                                                            |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPLICATION_USER_MODEL_ID_MAX_LENGTH"></span><span id="application_user_model_id_max_length"></span><dl> <dt>**APLICATIVO \_ TAMANHO \_ MÁXIMO \_ DA ID DO MODELO DE \_ \_ USUÁRIO**</dt> <dt>130</dt> </dl>                  | O comprimento máximo da ID do modelo de usuário do aplicativo. O espaço está incluído para o terminador NULL.<br/>                             |
| <span id="APPLICATION_USER_MODEL_ID_MIN_LENGTH"></span><span id="application_user_model_id_min_length"></span><dl> <dt>**APLICATIVO \_ COMPRIMENTO \_ MÍNIMO \_ DA ID DO MODELO DE \_ \_ USUÁRIO**</dt> <dt>21</dt> </dl>                   | O comprimento mínimo da ID do modelo de usuário do aplicativo. O espaço está incluído para o terminador NULL.<br/>                             |
| <span id="PACKAGE_ARCHITECTURE_MAX_LENGTH"></span><span id="package_architecture_max_length"></span><dl> <dt>**PACOTE \_ ARQUITETURA \_ COMPRIMENTO \_ MÁXIMO**</dt> <dt>7</dt> </dl>                                     | O comprimento máximo da arquitetura. Nenhum espaço incluído para o terminador NULL.<br/>                                          |
| <span id="PACKAGE_ARCHITECTURE_MIN_LENGTH"></span><span id="package_architecture_min_length"></span><dl> <dt>**PACOTE \_ COMPRIMENTO \_ MÍNIMO \_ DA ARQUITETURA**</dt> <dt>3</dt> </dl>                                     | O comprimento mínimo da arquitetura. Nenhum espaço incluído para o terminador NULL.<br/>                                          |
| <span id="PACKAGE_FAMILY_NAME_MAX_LENGTH"></span><span id="package_family_name_max_length"></span><dl> <dt>**PACOTE \_ COMPRIMENTO \_ MÁXIMO DO NOME DA \_ \_ FAMÍLIA**</dt> <dt>64</dt> </dl>                                      | O comprimento máximo do nome da família. Nenhum espaço incluído para o terminador NULL.<br/>                                           |
| <span id="PACKAGE_FAMILY_NAME_MIN_LENGTH"></span><span id="package_family_name_min_length"></span><dl> <dt>**PACOTE \_ COMPRIMENTO \_ MÍNIMO DO NOME DA \_ \_ FAMÍLIA**</dt> <dt>17</dt> </dl>                                      | O comprimento mínimo do nome da família. Nenhum espaço incluído para o terminador NULL.<br/>                                           |
| <span id="PACKAGE_FULL_NAME_MAX_LENGTH"></span><span id="package_full_name_max_length"></span><dl> <dt>**PACOTE \_ COMPRIMENTO \_ MÁXIMO DE NOME \_ \_ COMPLETO**</dt> <dt>127</dt> </dl>                                           | O comprimento máximo do nome completo. Nenhum espaço incluído para o terminador NULL.<br/>                                             |
| <span id="PACKAGE_FULL_NAME_MIN_LENGTH"></span><span id="package_full_name_min_length"></span><dl> <dt>**PACOTE \_ COMPRIMENTO \_ MÍNIMO DE NOME \_ \_ COMPLETO**</dt> <dt>30</dt> </dl>                                            | O comprimento mínimo do nome completo. Nenhum espaço incluído para o terminador NULL.<br/>                                             |
| <span id="PACKAGE_NAME_MAX_LENGTH"></span><span id="package_name_max_length"></span><dl> <dt>**PACOTE \_ TAMANHO \_ MÁXIMO \_ DO NOME**</dt> <dt>50</dt> </dl>                                                            | O comprimento máximo do nome. Nenhum espaço incluído para o terminador NULL.<br/>                                                  |
| <span id="PACKAGE_NAME_MIN_LENGTH"></span><span id="package_name_min_length"></span><dl> <dt>**PACOTE \_ NAME \_ MIN \_ LENGTH**</dt> <dt>3</dt> </dl>                                                             | O comprimento mínimo do nome. Nenhum espaço incluído para o terminador NULL.<br/>                                                  |
| <span id="PACKAGE_PUBLISHERID_MAX_LENGTH"></span><span id="package_publisherid_max_length"></span><dl> <dt>**PACOTE \_ PUBLISHERID \_ COMPRIMENTO \_ MÁXIMO**</dt> <dt>13</dt> </dl>                                       | O comprimento máximo da ID do editor. Nenhum espaço incluído para o terminador NULL.<br/>                                          |
| <span id="PACKAGE_PUBLISHERID_MIN_LENGTH"></span><span id="package_publisherid_min_length"></span><dl> <dt>**PACOTE \_ PUBLISHERID \_ MIN \_ LENGTH**</dt> <dt>13</dt> </dl>                                       | O comprimento mínimo da ID do editor. Nenhum espaço incluído para o terminador NULL.<br/>                                          |
| <span id="PACKAGE_PUBLISHER_MAX_LENGTH"></span><span id="package_publisher_max_length"></span><dl> <dt>**PACOTE \_ COMPRIMENTO \_ MÁXIMO \_ DO PUBLICADOR**</dt> <dt>8192</dt> </dl>                                           | O comprimento máximo do publicador. Por exemplo, CN=*publicador*. Nenhum espaço incluído para o terminador NULL.<br/>                |
| <span id="PACKAGE_PUBLISHER_MIN_LENGTH"></span><span id="package_publisher_min_length"></span><dl> <dt>**PACOTE \_ COMPRIMENTO \_ MÍNIMO \_ DO PUBLICADOR**</dt> <dt>4</dt> </dl>                                              | O comprimento mínimo do publicador. Nenhum espaço incluído para o terminador NULL.<br/>                                             |
| <span id="PACKAGE_RELATIVE_APPLICATION_ID_MAX_LENGTH"></span><span id="package_relative_application_id_max_length"></span><dl> <dt>**PACOTE \_ COMPRIMENTO \_ MÁXIMO \_ DA ID DO APLICATIVO \_ \_ RELATIVO**</dt> <dt>65</dt> </dl> | O comprimento máximo da ID do aplicativo relativo do pacote. O espaço está incluído para o terminador NULL.<br/>                       |
| <span id="PACKAGE_RELATIVE_APPLICATION_ID_MIN_LENGTH"></span><span id="package_relative_application_id_min_length"></span><dl> <dt>**PACOTE \_ COMPRIMENTO \_ MÍNIMO \_ DA ID DO APLICATIVO \_ \_ RELATIVO**</dt> <dt>2</dt> </dl>  | O comprimento mínimo da ID do aplicativo relativo do pacote. O espaço está incluído para o terminador NULL.<br/>                       |
| <span id="PACKAGE_RESOURCEID_MAX_LENGTH"></span><span id="package_resourceid_max_length"></span><dl> <dt>**PACOTE \_ COMPRIMENTO MÁXIMO \_ \_ DE RESOURCEID**</dt> <dt>30</dt> </dl>                                          | O comprimento máximo da ID do recurso. Nenhum espaço incluído para o terminador NULL.<br/>                                           |
| <span id="PACKAGE_RESOURCEID_MIN_LENGTH"></span><span id="package_resourceid_min_length"></span><dl> <dt>**PACOTE \_ RESOURCEID \_ MIN \_ LENGTH**</dt> <dt>0</dt> </dl>                                           | O comprimento mínimo da ID do recurso. Nenhum espaço incluído para o terminador NULL.<br/>                                           |
| <span id="PACKAGE_VERSION_MAX_LENGTH"></span><span id="package_version_max_length"></span><dl> <dt>**PACOTE \_ COMPRIMENTO \_ MÁXIMO \_ DA VERSÃO**</dt> <dt>23</dt> </dl>                                                   | O comprimento máximo da versão. Por exemplo, *xxxxx*. *xxxxx*. *xxxxx*. *xxxxx*. Nenhum espaço incluído para o terminador NULL/<br/> |
| <span id="PACKAGE_VERSION_MIN_LENGTH"></span><span id="package_version_min_length"></span><dl> <dt>**PACOTE \_ COMPRIMENTO \_ MÍNIMO \_ DA VERSÃO**</dt> <dt>7</dt> </dl>                                                    | O comprimento mínimo da versão. Por exemplo, *x*. *x*. *x*. *x*. Nenhum espaço incluído para o terminador NULL.<br/>                 |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>AppModel.h</dt> </dl> |



 

 





