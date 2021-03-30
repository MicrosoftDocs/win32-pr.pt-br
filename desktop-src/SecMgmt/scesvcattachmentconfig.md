---
description: A função SceSvcAttachmentConfig é chamada pelo mecanismo de configuração de segurança quando o sistema é configurado.
ms.assetid: ad20649a-2391-421b-a08c-a4ea6a882abc
title: Função de retorno de chamada SceSvcAttachmentConfig
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SceSvcAttachmentConfig
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: c78caa3b8e08ade9c674a11d113a8b91b8f5fad1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646992"
---
# <a name="scesvcattachmentconfig-callback-function"></a>Função de retorno de chamada SceSvcAttachmentConfig

A função **SceSvcAttachmentConfig** é chamada pelo mecanismo de configuração de segurança quando o sistema é configurado.

## <a name="syntax"></a>Sintaxe


```C++
SCESTATUS WINAPI SceSvcAttachmentConfig(
  _In_ PSCESVC_CALLBACK_INFO pSceCbInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSceCbInfo* \[ no\]
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ informações de retorno de chamada SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) que contém o identificador de banco de dados e as funções de retorno de chamada para consultar, definir e liberar informações.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se essa função for bem-sucedida, ela retornará SCESTATUS \_ Success. Caso contrário, ele retorna um código de erro. Para obter mais informações sobre os códigos de erro de configuração de segurança, consulte [valores de retorno de anexo](management-return-values.md).

## <a name="remarks"></a>Comentários

Ao implementar essa função, use a função de retorno de chamada apontada pelo membro **pfQueryInfo** da estrutura de [**\_ \_ informações de retorno de chamada SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfQueryInfo) para recuperar informações de configuração. Em seguida, configure o serviço usando as informações retornadas.

Essa função deve fazer o seguinte:

-   Consultar informações de configuração do conjunto de ferramentas de configuração de segurança usando a função de retorno de chamada apontada pelo membro **pfQueryInfo** da estrutura de [**informações de retorno de \_ chamada \_ SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfQueryInfo).
-   Configure o serviço usando as informações de configuração.

Para obter mais informações, consulte [Implementing SceSvcAttachmentConfig](implementing-scesvcattachmentconfig.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**informações de retorno de chamada do SCESVC \_ \_**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)
</dt> <dt>

[**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md)
</dt> </dl>

 

 




