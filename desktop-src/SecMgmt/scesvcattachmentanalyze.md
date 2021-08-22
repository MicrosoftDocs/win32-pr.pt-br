---
description: A função SceSvcAttachmentAnalyze é chamada pelo Mecanismo de Configuração de Segurança quando o sistema é analisado.
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
ms.openlocfilehash: 9bb84cc6a8492c729926b644a246b8ee8a03e1de4c2eae6e3de1fd88c5ba339f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004914"
---
# <a name="scesvcattachmentanalyze-callback-function"></a>Função de retorno de chamada SceSvcAttachmentAnalyze

A **função SceSvcAttachmentAnalyze** é chamada pelo Mecanismo de Configuração de Segurança quando o sistema é analisado.

## <a name="syntax"></a>Sintaxe


```C++
SCESTATUS WINAPI SceSvcAttachmentAnalyze(
  _In_ PSCESVC_CALLBACK_INFO pSceCbInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSceCbInfo* \[ Em\]
</dt> <dd>

Ponteiro para uma estrutura DE INFORMAÇÕES DE RETORNO DE CHAMADA [**SCESVC \_ \_**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) que contém um ponteiro de função de retorno de chamada e um handle de banco de dados opaco para consultar, definir e liberar informações.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se essa função for bem-sucedida, ela retornará SCESTATUS \_ SUCCESS. Caso contrário, retornará um código de erro. Para obter mais informações sobre os códigos de erro de Configuração de Segurança, consulte [Valores de retorno de anexo.](management-return-values.md)

## <a name="remarks"></a>Comentários

A **função SceSvcAttachmentAnalyze** deve fazer o seguinte:

-   Consulte diretamente as informações de configuração do serviço.
-   Chame a função de retorno de chamada apontada pelo membro **pfQueryInfo** da estrutura [**SCESVC \_ CALLBACK \_ INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfQueryInfo) para recuperar informações do banco de dados de segurança.
-   Compute as diferenças entre as informações com base no tipo e na sintaxe.
-   Chame a função de retorno de chamada apontada pelo membro **pfSetInfo** da estrutura [**SCESVC \_ CALLBACK \_ INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfSetInfo) para atualizar o banco de dados de segurança com as informações de serviço recuperadas que são diferentes.

Para obter mais informações, [consulte Implementando SceSvcAttachmentAnalyze](implementing-scesvcattachmentanalyze.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Implementando SceSvcAttachmentAnalyze](implementing-scesvcattachmentanalyze.md)
</dt> <dt>

[**INFORMAÇÕES DE RETORNO DE CHAMADA DO SCESVC \_ \_**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)
</dt> <dt>

[**SceSvcAttachmentConfig**](scesvcattachmentconfig.md)
</dt> </dl>

 

 




