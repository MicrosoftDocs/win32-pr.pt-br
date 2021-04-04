---
description: A função SceSvcAttachmentAnalyze é chamada pelo mecanismo de configuração de segurança quando o sistema é analisado.
ms.assetid: 8e8a39b9-c4e2-446e-8e0c-eb2113234c1a
title: Função de retorno de chamada SceSvcAttachmentAnalyze
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SceSvcAttachmentAnalyze
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 296d755a0b082b46122432936d30614019b8b9a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646993"
---
# <a name="scesvcattachmentanalyze-callback-function"></a>Função de retorno de chamada SceSvcAttachmentAnalyze

A função **SceSvcAttachmentAnalyze** é chamada pelo mecanismo de configuração de segurança quando o sistema é analisado.

## <a name="syntax"></a>Sintaxe


```C++
SCESTATUS WINAPI SceSvcAttachmentAnalyze(
  _In_ PSCESVC_CALLBACK_INFO pSceCbInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSceCbInfo* \[ no\]
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ informações de retorno de chamada SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) que contém um identificador de banco de dados opaco e ponteiros de função de retorno de chamada para consultar, definir e informações gratuitas.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se essa função for bem-sucedida, ela retornará SCESTATUS \_ Success. Caso contrário, ele retorna um código de erro. Para obter mais informações sobre os códigos de erro de configuração de segurança, consulte [valores de retorno de anexo](management-return-values.md).

## <a name="remarks"></a>Comentários

A função **SceSvcAttachmentAnalyze** deve fazer o seguinte:

-   Consulte diretamente as informações de configuração do serviço.
-   Chame a função de retorno de chamada apontada pelo membro **pfQueryInfo** da estrutura de [**\_ \_ informações de retorno de chamada SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfQueryInfo) para recuperar informações do banco de dados de segurança.
-   Computar as diferenças entre as informações com base no tipo e na sintaxe.
-   Chame a função de retorno de chamada apontada pelo membro **pfSetInfo** da estrutura de [**\_ \_ informações de retorno de chamada SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfSetInfo) para atualizar o banco de dados de segurança com as informações de serviço recuperadas que são diferentes.

Para obter mais informações, consulte [Implementing SceSvcAttachmentAnalyze](implementing-scesvcattachmentanalyze.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Implementando SceSvcAttachmentAnalyze](implementing-scesvcattachmentanalyze.md)
</dt> <dt>

[**informações de retorno de chamada do SCESVC \_ \_**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)
</dt> <dt>

[**SceSvcAttachmentConfig**](scesvcattachmentconfig.md)
</dt> </dl>

 

 




