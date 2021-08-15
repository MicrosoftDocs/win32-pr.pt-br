---
title: Função MrmDestroyIndexerAndMessages (MrmResourceIndexer. h)
description: Libera recursos de máquina associados a um indexador de recurso.
ms.assetid: AD770F40-BEDB-46C3-9527-DC46169C6193
keywords:
- Menus de função MrmDestroyIndexerAndMessages e outros recursos
topic_type:
- apiref
api_name:
- MrmDestroyIndexerAndMessages
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a16dd8c03fdf4b89f734cf45c5ede0d2a55d377fae52e1a52139f82a0dcdf654
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118733656"
---
# <a name="mrmdestroyindexerandmessages-function"></a>Função MrmDestroyIndexerAndMessages

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, quanto às informações fornecidas aqui.\]

Libera recursos de máquina associados a um indexador de recurso. Destrói o identificador, libera o indexador e exclui todas as mensagens. Para obter mais informações e orientações baseadas em cenários de como usar essas APIs, consulte APIs de [Pri (indexação de recursos de pacote) e sistemas de compilação personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT HRESULT MrmDestroyIndexerAndMessages(
  _In_ MrmResourceIndexerHandle indexer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*indexador* \[ no\]
</dt> <dd>

Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**

Um identificador que identifica o indexador de recursos a ser destruído.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

S \_ OK se a função for bem-sucedida, caso contrário, algum outro valor. Use as macros SUCCEEDed () ou FAILED () (definidas em Winerror. h) para determinar o êxito ou a falha.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, \[ somente aplicativos da área de trabalho da versão 1803\]<br/>                                       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor\]<br/>                                                 |
| parâmetro<br/>                   | <dl> <dt>MrmResourceIndexer. h</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Mrmsupport. lib</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Mrmsupport.dll</dt> </dl>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[APIs de PRI (índice de recurso do pacote) e sistemas de build personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

