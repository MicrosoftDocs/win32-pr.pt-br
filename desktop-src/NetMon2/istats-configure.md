---
description: O método configure envia informações de configuração de captura.
ms.assetid: 739ed1df-1a84-4c48-a1ac-2dba7a614cdd
title: 'Método IStats:: Configure (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 357d0dd9dbb6e0f57a7ecd3dffcec4c0d1e546ce0bc058ce0144796ca8836113
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364963"
---
# <a name="istatsconfigure-method"></a>Método IStats:: Configure

O método **Configure** envia informações de configuração de captura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT STDMETHODCALLTYPE Configure(
  [in]  HBLOB hConfigurationBlob,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hConfigurationBlob* \[ no\]
</dt> <dd>

Identificador para o BLOB que o chamador configura.

</dd> <dt>

*hErrorBlob* \[ fora\]
</dt> <dd>

Identificador para um BLOB de erro que contém informações adicionais sobre o erro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.

Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:



| Código de retorno                                                                                                         | Descrição                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_cadeia de blob NMERR \_ \_ inválida**</dt> </dl>         | A cadeia de caracteres não é terminada em nulo.<br/>                                                                                                                                                                                            |
| <dl> <dt>**\_blob NMERR \_ não \_ inicializado**</dt> </dl>        | O método **createBlob** não foi chamado.<br/>                                                                                                                                                                                |
| <dl> <dt>**NMERR \_ \_ blob inválido**</dt> </dl>                 | O objeto que é apontado não é um BLOB.<br/>                                                                                                                                                                                  |
| <dl> <dt>**BLOB de upNMERR de \_ nível \_**</dt> </dl>                 | O número de versão do BLOB está incorreto.<br/>                                                                                                                                                                                         |
| <dl> <dt>**a \_ entrada de blob NMERR \_ \_ já \_ existe**</dt> </dl>  | Já existe uma entrada de BLOB.<br/>                                                                                                                                                                                                  |
| <dl> <dt>**a \_ entrada de blob NMERR não \_ \_ \_ \_ existe**</dt> </dl> | O BLOB de configuração especificado pelo parâmetro *hConfigurationBlob* não tem uma entrada necessária para executar esta operação. Examine o BLOB de erro retornado pelo parâmetro *hErrorBlob* para determinar qual entrada não foi encontrada.<br/> |
| <dl> <dt>**\_ \_ especificador ambíguo NMERR**</dt> </dl>          | O BLOB não tem informações de proprietário ou categoria.<br/>                                                                                                                                                                                 |
| <dl> <dt>**\_proprietário do blob NMERR \_ \_ não \_ encontrado**</dt> </dl>       | A seção de proprietário do BLOB não foi encontrada.<br/>                                                                                                                                                                                  |
| <dl> <dt>**\_categoria de blob NMERR \_ \_ não \_ encontrada**</dt> </dl>    | A seção de categoria do BLOB não foi encontrada.<br/>                                                                                                                                                                               |
| <dl> <dt>**NMERR \_ \_ categoria desconhecida**</dt> </dl>             | Informações de categoria foram encontradas, mas não compreendidas.<br/>                                                                                                                                                                            |
| <dl> <dt>**\_marca desconhecida \_ NMERR**</dt> </dl>                  | Informações de marca foram encontradas, mas não compreendidas.<br/>                                                                                                                                                                                 |
| <dl> <dt>**\_erro de \_ conversão de blob NMERR \_**</dt> </dl>       | O BLOB está corrompido.<br/>                                                                                                                                                                                                          |
| <dl> <dt>**NMERR \_ \_ gatilho ilegal**</dt> </dl>              | A parte do gatilho do BLOB está corrompida.<br/>                                                                                                                                                                                   |



 

## <a name="remarks"></a>Comentários

Você deve aplicar esse método para reiniciar um NPP que foi iniciado, interrompido, mas não desconectado.

O BLOB de erro retornado por *hErrorBlob* contém entradas que monitor de rede não pôde entender ou localizar no blob de configuração especificado no parâmetro *hConfigurationBlob* . O BLOB de erro retornado contém informações de erro que o aplicativo pode usar para solução de problemas. Por exemplo, se \_ a entrada de blob NMERR não \_ \_ \_ \_ existir for retornada, a entrada monitor de rede não poderá localizar é incluída no blob de erros retornado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IStats](istats.md)
</dt> <dt>

[ISTATS:: Conexão](istats-connect.md)
</dt> <dt>

[BLOBs de Monitor de Rede](network-monitor-blobs.md)
</dt> </dl>

 

 




