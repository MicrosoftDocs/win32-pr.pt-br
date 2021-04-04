---
description: A função SceSvcAttachmentUpdate é chamada pelos snap-ins de configuração de segurança para passar alterações de configuração para o banco de dados de segurança.
ms.assetid: 2b5b3718-8ccb-480a-97fb-c8115d8f3a5c
title: Função de retorno de chamada SceSvcAttachmentUpdate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SceSvcAttachmentUpdate
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 5bc4c9426f6a085c72f2fc3d872de4d7da59156b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646991"
---
# <a name="scesvcattachmentupdate-callback-function"></a>Função de retorno de chamada SceSvcAttachmentUpdate

A função **SceSvcAttachmentUpdate** é chamada pelos snap-ins de configuração de segurança para passar alterações de configuração para o banco de dados de segurança.

## <a name="syntax"></a>Sintaxe


```C++
SCESTATUS WINAPI SceSvcAttachmentUpdate(
  _In_ PSCESVC_CALLBACK_INFO     pSceCbInfo,
  _In_ SCESVC_CONFIGURATION_INFO *ServiceInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSceCbInfo* \[ no\]
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ informações de retorno de chamada SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) que contém o identificador de retorno de chamada e ponteiros de função para o SCE.

</dd> <dt>

*Informações* \[ no\]
</dt> <dd>

Informações de configuração atualizadas. A estrutura de dados usada para essas informações são as [**\_ \_ informações de configuração do SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_info).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se essa função for bem-sucedida, ela retornará SCESTATUS \_ Success. Caso contrário, ele retorna um código de erro. Para obter mais informações sobre os códigos de erro de configuração de segurança, consulte [valores de retorno de anexo](management-return-values.md).

## <a name="remarks"></a>Comentários

A função **SceSvcAttachmentUpdate** deve fazer o seguinte:

-   Chame a função de retorno de chamada apontada pelo membro **pfQueryInfo** da estrutura de [**\_ \_ informações de retorno de chamada SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfQueryInfo) para recuperar as informações de configuração de base atuais do banco de dados de segurança.
-   Chame a função de retorno de chamada apontada pelo membro **pfQueryInfo** da estrutura de [**\_ \_ informações de retorno de chamada SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfQueryInfo) para recuperar o último conjunto de diferenças (informações de análise) do banco de dados de segurança.
-   Use as informações de serviço fornecidas (consulte *serviceInfo*) para calcular a nova configuração de base.
-   Use as informações de serviço fornecidas (consulte *serviceInfo*) e a análise para calcular as novas informações de diferença.
-   Chame a função de retorno de chamada apontada pelo membro **pfSetInfo** da estrutura de [**\_ \_ informações de retorno de chamada SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfSetInfo) para definir a nova configuração de base no banco de dados de segurança.
-   Chame a função de retorno de chamada apontada pelo membro **pfSetInfo** da estrutura de [**\_ \_ informações de retorno de chamada SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfSetInfo) para definir as novas informações de análise no banco de dados de segurança.

Para obter mais informações, consulte [Implementing SceSvcAttachmentUpdate](implementing-scesvcattachmentupdate.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**informações de retorno de chamada do SCESVC \_ \_**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)
</dt> <dt>

[**\_informações de configuração do SCESVC \_**](/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_info)
</dt> </dl>

 

 




