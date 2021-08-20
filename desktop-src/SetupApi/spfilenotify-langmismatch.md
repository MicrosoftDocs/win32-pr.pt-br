---
description: A \_ notificação SPFILENOTIFY LANGMISMATCH será enviada para a rotina de retorno de chamada se o idioma do arquivo a ser copiado não corresponder ao idioma de um arquivo de destino existente.
ms.assetid: dff3969e-5847-4ad5-b7d4-237144bbe8e6
title: Mensagem de SPFILENOTIFY_LANGMISMATCH (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50cae8788e3ffac2de5cc7fc115b9363b8ad4591a0a4dd2447a3f86f735bec1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117964464"
---
# <a name="spfilenotify_langmismatch-message"></a>\_Mensagem SPFILENOTIFY LANGMISMATCH

A notificação **SPFILENOTIFY \_ LANGMISMATCH** será enviada para a rotina de retorno de chamada se o idioma do arquivo a ser copiado não corresponder ao idioma de um arquivo de destino existente. Ele pode ser enviado para a rotina de retorno de chamada isoladamente ou combinada, usando o operador OR, com [**SPFILENOTIFY \_ TARGETEXISTS**](spfilenotify-targetexists.md) e/ou [**SPFILENOTIFY \_ TARGETNEWER**](spfilenotify-targetnewer.md).


```C++
SPFILENOTIFY_LANGMISMATCH
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) LanguageInfo;
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Param1* 
</dt> <dd>

Ponteiro para uma estrutura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) que contém informações sobre os caminhos dos arquivos de origem e de destino.

</dd> <dt>

*Param2* 
</dt> <dd>

Identifica os idiomas incompatíveis. Esse membro tem o identificador de idioma do arquivo de origem na palavra inferior e o identificador de idioma do arquivo de destino existente na palavra alta.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

A rotina de retorno de chamada deve retornar um dos valores a seguir.



| Código de retorno                                                                          | Descrição                                                             |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**TRUE**</dt> </dl>  | Copie o arquivo e substitua o arquivo existente.<br/>               |
| <dl> <dt>**FOR**</dt> </dl> | Ignore a operação de cópia. Não substitua o arquivo existente.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Setupapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral](overview.md)
</dt> <dt>

[Notificações](notifications.md)
</dt> <dt>

[**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> <dt>

[**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




