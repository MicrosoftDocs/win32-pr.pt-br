---
title: Constantes de identidade (AppModel. h)
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
ms.openlocfilehash: 681a0aef767afe92cdb93eee3849df8ed6a5f080
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105790580"
---
# <a name="identity-constants"></a>Constantes de identidade

Especifica o comprimento das cadeias de caracteres para os campos de identidade do pacote. O comprimento é medido em caracteres e pode ou não incluir espaço para o terminador nulo.

> [!Note]  
> As constantes no formato: **\_ \_ \_ \_ \* \_ tamanho da ID do modelo de usuário do aplicativo** e **\_ \_ \_ \_ \* \_ comprimento da ID do aplicativo relativo do pacote** incluem espaço para um terminador nulo, mas constantes no formato: o **\_ \* \_ tamanho do pacote** não inclui espaço para um terminador nulo.

 



| Constante/valor                                                                                                                                                                                                                                                                                                   | Descrição                                                                                                                            |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPLICATION_USER_MODEL_ID_MAX_LENGTH"></span><span id="application_user_model_id_max_length"></span><dl> Do <dt>**aplicativo \_ \_ \_ \_ \_ Comprimento máximo da ID de modelo do usuário**</dt> <dt>130</dt> </dl>                  | O comprimento máximo da ID do modelo de usuário do aplicativo. O espaço está incluído para o terminador nulo.<br/>                             |
| <span id="APPLICATION_USER_MODEL_ID_MIN_LENGTH"></span><span id="application_user_model_id_min_length"></span><dl> Do <dt>**aplicativo \_ ID de modelo de usuário com \_ \_ \_ \_ comprimento mínimo**</dt> <dt>21</dt> </dl>                   | O comprimento mínimo da ID do modelo de usuário do aplicativo. O espaço está incluído para o terminador nulo.<br/>                             |
| <span id="PACKAGE_ARCHITECTURE_MAX_LENGTH"></span><span id="package_architecture_max_length"></span><dl> <dt>**Pacote \_ do \_ \_ Tamanho máximo da arquitetura**</dt> <dt>7</dt> </dl>                                     | O comprimento máximo da arquitetura. Nenhum espaço incluído para o terminador nulo.<br/>                                          |
| <span id="PACKAGE_ARCHITECTURE_MIN_LENGTH"></span><span id="package_architecture_min_length"></span><dl> <dt>**Pacote \_ do \_ \_ Tamanho mínimo de arquitetura**</dt> <dt>3</dt> </dl>                                     | O comprimento mínimo da arquitetura. Nenhum espaço incluído para o terminador nulo.<br/>                                          |
| <span id="PACKAGE_FAMILY_NAME_MAX_LENGTH"></span><span id="package_family_name_max_length"></span><dl> <dt>**Pacote \_ do \_ \_ \_ Tamanho máximo do nome da família**</dt> <dt>64</dt> </dl>                                      | O comprimento máximo do nome da família. Nenhum espaço incluído para o terminador nulo.<br/>                                           |
| <span id="PACKAGE_FAMILY_NAME_MIN_LENGTH"></span><span id="package_family_name_min_length"></span><dl> <dt>**Pacote \_ do Nome da família- \_ \_ \_ tamanho mínimo**</dt> <dt>17</dt> </dl>                                      | O comprimento mínimo do nome da família. Nenhum espaço incluído para o terminador nulo.<br/>                                           |
| <span id="PACKAGE_FULL_NAME_MAX_LENGTH"></span><span id="package_full_name_max_length"></span><dl> <dt>**Pacote \_ do \_ \_ \_ Tamanho máximo de nome completo**</dt> <dt>127</dt> </dl>                                           | O comprimento máximo do nome completo. Nenhum espaço incluído para o terminador nulo.<br/>                                             |
| <span id="PACKAGE_FULL_NAME_MIN_LENGTH"></span><span id="package_full_name_min_length"></span><dl> <dt>**Pacote \_ do \_ \_ \_ Comprimento mínimo de nome completo**</dt> <dt>30</dt> </dl>                                            | O comprimento mínimo do nome completo. Nenhum espaço incluído para o terminador nulo.<br/>                                             |
| <span id="PACKAGE_NAME_MAX_LENGTH"></span><span id="package_name_max_length"></span><dl> <dt>**Pacote \_ do \_ \_ Comprimento máximo do nome**</dt> <dt>50</dt> </dl>                                                            | O comprimento máximo do nome. Nenhum espaço incluído para o terminador nulo.<br/>                                                  |
| <span id="PACKAGE_NAME_MIN_LENGTH"></span><span id="package_name_min_length"></span><dl> <dt>**Pacote \_ do \_ \_ Comprimento mínimo de nome**</dt> <dt>3</dt> </dl>                                                             | O comprimento mínimo do nome. Nenhum espaço incluído para o terminador nulo.<br/>                                                  |
| <span id="PACKAGE_PUBLISHERID_MAX_LENGTH"></span><span id="package_publisherid_max_length"></span><dl> <dt>**Pacote \_ do PUBLISHERid \_ máx. \_ comprimento**</dt> <dt>13</dt> </dl>                                       | O comprimento máximo da ID do editor. Nenhum espaço incluído para o terminador nulo.<br/>                                          |
| <span id="PACKAGE_PUBLISHERID_MIN_LENGTH"></span><span id="package_publisherid_min_length"></span><dl> <dt>**Pacote \_ do PUBLISHERid \_ min \_ comprimento**</dt> <dt>13</dt> </dl>                                       | O comprimento mínimo da ID do editor. Nenhum espaço incluído para o terminador nulo.<br/>                                          |
| <span id="PACKAGE_PUBLISHER_MAX_LENGTH"></span><span id="package_publisher_max_length"></span><dl> <dt>**Pacote \_ do \_ \_ Comprimento máximo do publicador**</dt> <dt>8192</dt> </dl>                                           | O comprimento máximo do Publicador. Por exemplo, CN =*Publisher*. Nenhum espaço incluído para o terminador nulo.<br/>                |
| <span id="PACKAGE_PUBLISHER_MIN_LENGTH"></span><span id="package_publisher_min_length"></span><dl> <dt>**Pacote \_ do \_ \_ Comprimento mínimo**</dt> <dt>4</dt> do Publicador </dl>                                              | O comprimento mínimo do Publicador. Nenhum espaço incluído para o terminador nulo.<br/>                                             |
| <span id="PACKAGE_RELATIVE_APPLICATION_ID_MAX_LENGTH"></span><span id="package_relative_application_id_max_length"></span><dl> <dt>**Pacote \_ do \_ \_ \_ \_ Comprimento máximo da ID de aplicativo relativo**</dt> <dt>65</dt> </dl> | O comprimento máximo da ID de aplicativo relativa do pacote. O espaço está incluído para o terminador nulo.<br/>                       |
| <span id="PACKAGE_RELATIVE_APPLICATION_ID_MIN_LENGTH"></span><span id="package_relative_application_id_min_length"></span><dl> <dt>**Pacote \_ do ID de aplicativo relativo- \_ \_ \_ \_ comprimento mínimo**</dt> <dt>2</dt> </dl>  | O comprimento mínimo da ID de aplicativo relativa do pacote. O espaço está incluído para o terminador nulo.<br/>                       |
| <span id="PACKAGE_RESOURCEID_MAX_LENGTH"></span><span id="package_resourceid_max_length"></span><dl> <dt>**Pacote \_ do \_ \_ Comprimento máximo de ResourceId**</dt> <dt>30</dt> </dl>                                          | O comprimento máximo da ID de recurso. Nenhum espaço incluído para o terminador nulo.<br/>                                           |
| <span id="PACKAGE_RESOURCEID_MIN_LENGTH"></span><span id="package_resourceid_min_length"></span><dl> <dt>**Pacote \_ do \_ \_ Comprimento mínimo de ResourceId**</dt> <dt>0</dt> </dl>                                           | O comprimento mínimo da ID do recurso. Nenhum espaço incluído para o terminador nulo.<br/>                                           |
| <span id="PACKAGE_VERSION_MAX_LENGTH"></span><span id="package_version_max_length"></span><dl> <dt>**Pacote \_ do \_ \_ Comprimento máximo de versão**</dt> <dt>23</dt> </dl>                                                   | O comprimento máximo da versão. Por exemplo, *xxxxx*. *xxxxx*. *xxxxx*. *xxxxx*. Nenhum espaço incluído para o terminador nulo/<br/> |
| <span id="PACKAGE_VERSION_MIN_LENGTH"></span><span id="package_version_min_length"></span><dl> <dt>**Pacote \_ do \_ \_ Tamanho mínimo de versão**</dt> <dt>7</dt> </dl>                                                    | O comprimento mínimo da versão. Por exemplo, *x*. *x*. *x*. *x*. Nenhum espaço incluído para o terminador nulo.<br/>                 |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>AppModel. h</dt> </dl> |



 

 





