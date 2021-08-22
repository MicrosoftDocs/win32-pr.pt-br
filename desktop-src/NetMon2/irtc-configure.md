---
description: Envia dados de configuração para uma captura de dados.
ms.assetid: fb8c8ac8-cef4-45e0-bb06-3cf09c8ad9ac
title: 'Método IRTC:: Configure (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 8f70674d8e570a2640fe301179b21a9f48ec612a17de69e43bdf5c38db4e65af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063906"
---
# <a name="irtcconfigure-method"></a>Método IRTC:: Configure

O método [**Configure**](configure.md) envia dados de configuração para uma captura de dados.

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

Um identificador para o BLOB que é configurado pelo chamador.

</dd> <dt>

*hErrorBlob* \[ fora\]
</dt> <dd>

Um identificador para um BLOB de erro que contém dados de erro adicionais.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.

Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:



| Código de retorno                                                                                                         | Descrição                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_blob NMERR \_ não \_ inicializado**</dt> </dl>        | O método **createBlob** não foi chamado.<br/>                                                                                                                                                 |
| <dl> <dt>**NMERR \_ \_ blob inválido**</dt> </dl>                 | O objeto apontado não é um BLOB.<br/>                                                                                                                                                           |
| <dl> <dt>**BLOB de upNMERR de \_ nível \_**</dt> </dl>                 | O número de versão do BLOB está incorreto.<br/>                                                                                                                                                          |
| <dl> <dt>**a \_ entrada de blob NMERR \_ \_ já \_ existe**</dt> </dl>  | Duplicar BLOB.<br/>                                                                                                                                                                                |
| <dl> <dt>**a \_ entrada de blob NMERR não \_ \_ \_ \_ existe**</dt> </dl> | O BLOB de configuração especificado por *hConfigurationBlob* não tem uma entrada necessária para executar esta operação. Exiba o BLOB de erro retornado por *hErrorBlob* para determinar qual entrada não foi encontrada.<br/> |
| <dl> <dt>**\_ \_ especificador ambíguo NMERR**</dt> </dl>          | O proprietário do BLOB ou os dados da categoria estão ausentes.<br/>                                                                                                                                                    |
| <dl> <dt>**\_proprietário do blob NMERR \_ \_ não \_ encontrado**</dt> </dl>       | A seção de proprietário do BLOB não foi encontrada.<br/>                                                                                                                                                          |
| <dl> <dt>**\_categoria de blob NMERR \_ \_ não \_ encontrada**</dt> </dl>    | A seção de categoria de BLOB não foi encontrada.<br/>                                                                                                                                                       |
| <dl> <dt>**NMERR \_ \_ categoria desconhecida**</dt> </dl>             | A seção de categoria de BLOB foi encontrada, mas não compreendida.<br/>                                                                                                                                       |
| <dl> <dt>**\_marca desconhecida \_ NMERR**</dt> </dl>                  | A seção de marca de BLOB foi encontrada, mas não compreendida.<br/>                                                                                                                                            |
| <dl> <dt>**\_erro de \_ conversão de blob NMERR \_**</dt> </dl>       | O BLOB está corrompido.<br/>                                                                                                                                                                           |
| <dl> <dt>**NMERR \_ \_ gatilho ilegal**</dt> </dl>              | A parte do gatilho do BLOB está corrompida.<br/>                                                                                                                                                    |
| <dl> <dt>**\_cadeia de blob NMERR \_ \_ inválida**</dt> </dl>         | A cadeia de caracteres não é terminada em nulo.<br/>                                                                                                                                                             |



 

## <a name="remarks"></a>Comentários

Você deve aplicar esse método para reiniciar um NPP que tenha sido iniciado, interrompido, mas não desconectado.

O BLOB de erro retornado por *hErrorBlob* contém entradas que monitor de rede não pôde entender ou localizar no blob de configuração especificado em *hConfigurationBlob*. O BLOB de erro retornado contém dados de erro que o aplicativo pode usar para solução de problemas. Por exemplo, se \_ a entrada de blob NMERR não \_ \_ \_ \_ existir for retornada, a entrada monitor de rede não poderá localizar será incluída no blob de erros retornado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[IRTC:: Conexão](irtc-connect.md)
</dt> <dt>

[BLOBs de Monitor de Rede](network-monitor-blobs.md)
</dt> </dl>

 

 




