---
description: Fornece acesso à memória compartilhada entre threads do Tablet.
ms.assetid: 047ff598-7d20-49d7-bdd3-498fe5c778c6
title: 'Método ITabletContextP:: UseSharedMemoryCommunications'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.UseSharedMemoryCommunications
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: d7880e1d0377d9d0140a0c82509abd31182c724e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105815569"
---
# <a name="itabletcontextpusesharedmemorycommunications-method"></a>Método ITabletContextP:: UseSharedMemoryCommunications

Fornece acesso à memória compartilhada entre threads do Tablet.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT UseSharedMemoryCommunications(
  [in]  DWORD pid,
  [out] DWORD *phEventMoreData,
  [out] DWORD *phEventClientReady,
  [out] DWORD *phMutexAccess,
  [out] DWORD *phFileMapping
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pid* \[ no\]
</dt> <dd>

ID do processo.

</dd> <dt>

*phEventMoreData* \[ fora\]
</dt> <dd>

Identificador de evento que sinaliza quando novos dados estão disponíveis para serem processados.

</dd> <dt>

*phEventClientReady* \[ fora\]
</dt> <dd>

O identificador de evento retornado usado para sinalizar que o cliente está pronto para receber dados. Sinalizado após o processamento de novos dados.

</dd> <dt>

*phMutexAccess* \[ fora\]
</dt> <dd>

O mutex que concede acesso à memória compartilhada.

</dd> <dt>

*phFileMapping* \[ fora\]
</dt> <dd>

Ponteiro para o bloco de memória compartilhada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                            | Descrição                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Êxito.<br/>                       |
| <dl> <dt>**E \_ falha**</dt> </dl> | Ocorreu um erro não especificado.<br/> |



 

## <a name="remarks"></a>Comentários

O método **UseSharedMemoryCommunications** é usado como parte do protocolo de memória compartilhada do Tablet PC. Como o serviço Wisptis tem um IL (nível de integridade alta), ele pode armazenar e acessar dados armazenados na memória compartilhada sem a necessidade de elevar seus privilégios.

A estrutura de [**\_ cabeçalho SHAREDMEMORY**](sharedmemory-header.md) é convertida dos dados referenciados pelo mapeamento de arquivo e os dados de pacote brutos seguem o **\_ cabeçalho SHAREDMEMORY**. Os dados brutos do pacote podem ser lidos da memória compartilhada quando o evento referenciado por *pdwEventClientReady* é gerado.

A lista a seguir descreve a sequência de eventos para acessar e usar a memória compartilhada.

-   O cliente define o evento clientReady.
-   O cliente aguarda o evento moreData.
-   O cliente adquire o mutex.
-   O cliente lê os dados de pacote da seção de memória compartilhada após o cabeçalho e os números de série após os pacotes.
-   O cliente manipula os dados dependendo do valor de **dwEvent**.
-   O cliente grava-1 (0xFFFFFFFF) em **dwEvent**.
-   O cliente libera o mutex.
-   O cliente define o evento clientReady.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                          |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface ITabletContextP**](itabletcontextp.md)
</dt> <dt>

[**UseNamedSharedMemoryCommunications**](itabletcontextp-usenamedsharedmemorycommunications.md)
</dt> </dl>

 

 




