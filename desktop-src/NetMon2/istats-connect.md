---
description: 'método IStats:: Conexão-o método Conexão conecta o NPP à rede usando uma NIC especificada e fornece informações de configuração para a conexão.'
ms.assetid: 29a12df7-9c81-40ff-ac12-33ce1de833b1
title: 'método IStats:: Conexão (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Connect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: e6521e77453ec77f81422c7903b1a394512a4c1b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471182"
---
# <a name="istatsconnect-method"></a>método IStats:: Conexão

o método **Conexão** conecta o NPP à rede usando uma NIC especificada e fornece informações de configuração para a conexão.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT STDMETHODCALLTYPE Connect(
  [in]  HBLOB  hInputBlob,
  [in]  LPVOID StatusCallbackProc,
  [in]  LPVOID UserContext,
  [out] HBLOB  hErrorBlob
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hInputBlob* \[ no\]
</dt> <dd>

Identificador para o BLOB que especifica a NIC à qual o NPP se conecta e as informações de configuração para essa conexão.

</dd> <dt>

*StatusCallbackProc* \[ no\]
</dt> <dd>

Endereço da função de retorno de chamada do usuário, que recebe atualizações de status, como gatilhos. Se uma função de retorno de chamada não for usada, defina esse parâmetro e o parâmetro *userContext* como **NULL**.

</dd> <dt>

*UserContext* \[ no\]
</dt> <dd>

Valor passado quando a função de retorno de chamada do usuário é chamada. O valor desse parâmetro é normalmente o HWND ou um ponteiro ' this '. Se uma função de retorno de chamada não for especificada, defina esse parâmetro e o parâmetro *StatusCallbackProc* como **NULL**.

</dd> <dt>

*hErrorBlob* \[ fora\]
</dt> <dd>

Identificador para um BLOB de erro que contém informações adicionais sobre o erro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.

Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro (que incluem os erros retornados pela chamada interna **IStats:: Configure** ):




| Código de retorno | Descrição | 
|-------------|-------------|
| <dl><dt><strong>NMERR_ALREADY_CONNECTED</strong></dt></dl> | Esta instância do objeto COM NPP já está conectada à rede.<br /> | 
| <dl><dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt></dl> | O BLOB de configuração está corrompido. Esse erro é gerado pela chamada <strong>IStats:: Configure</strong> .<br /> | 
| <dl><dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt></dl> | O BLOB de entrada especificado pelo parâmetro <em>hInputBlob</em> não tem uma entrada necessária para executar esta operação. esse erro pode ser gerado pela chamada <strong>IStats:: Conexão</strong> ou <strong>IStats:: Configure</strong> . Examine o BLOB de erro retornado por <em>hErrorBlob</em> para determinar qual entrada não foi encontrada.<br /> | 
| <dl><dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt></dl> | A função <strong>createBlob</strong> não foi chamada. Esse erro é gerado pela chamada <strong>IStats:: Configure</strong> .<br /> | 
| <dl><dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt></dl> | A cadeia de caracteres não é terminada em nulo. Esse erro é gerado pela chamada <strong>IStats:: Configure</strong> .<br /> | 
| <dl><dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt></dl> | A parte do gatilho do BLOB de entrada está corrompida. Esse erro é gerado pela chamada <strong>IStats:: Configure</strong> .<br /> | 
| <dl><dt><strong>NMERR_INVALID_BLOB</strong></dt></dl> | O objeto especificado em <em>hInputBlob</em> não é um blob. Esse erro é gerado pela chamada <strong>IStats:: Configure</strong> .<br /> | 
| <dl><dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt></dl> | O diretório de captura padrão não foi definido no registro. Para definir o diretório de captura, use o caminho a seguir. <br /><pre class="syntax" data-space="preserve"><code>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\nm\Parameters\CapturePath</code></pre> | 
| <dl><dt><strong>NMERR_OUT_OF_MEMORY</strong></dt></dl> | A memória necessária para executar esta operação não estava disponível. Esse erro é gerado pela chamada <strong>IStats:: Configure</strong> .<br /> | 
| <dl><dt><strong>NMERR_TIMEOUT</strong></dt></dl> | O tempo limite da solicitação foi atingido. Esse erro é gerado pela chamada <strong>IStats:: Configure</strong> .<br /> | 
| <dl><dt><strong>NMERR_UPLEVEL_BLOB</strong></dt></dl> | O número de versão do BLOB especificado em <em>hInputBlob</em> está incorreto. Esse erro é gerado pela chamada <strong>IStats:: Configure</strong> .<br /> | 




 

## <a name="remarks"></a>Comentários

quando o método **Conexão** é chamado, Monitor de Rede chama automaticamente o método **IStats:: Configure** usando o BLOB fornecido pelo parâmetro *hInputBlob* . observe que todos os códigos de erro retornados pela chamada para **IStats:: Configure** são passados de volta e retornados pela chamada **IStats:: Conexão** .

Esse método deve ser chamado antes que você possa iniciar a captura de quadros. Observe que quando você se conecta à rede usando esse método, você deve continuar a usar a interface **IStats** para capturar quadros.

O BLOB de entrada especificado por *hInputBlob* pode ser obtido chamando os métodos **GetNPPBlobFromUI**, **GetNPPBlobTable** e **SelectNPPBlobFromTable** .

O BLOB de erro retornado pelo parâmetro *hErrorBlob* contém entradas que monitor de rede não pôde entender ou localizar no blob de entrada especificado em *hInputBlob*. O BLOB de erro retornado contém informações de erro que o aplicativo pode usar para solução de problemas. Por exemplo, se \_ a entrada de blob NMERR não \_ \_ \_ \_ existir for retornada, a entrada que monitor de rede não pôde localizar será incluída no blob de erros retornado.



| Para obter informações sobre                                             | Consulte                                                                          |
|-------------------------------------------------------------------|------------------------------------------------------------------------------|
| Obtendo o BLOB de entrada que representa uma placa de interface de rede | [Selecionando uma placa de interface de rede](selecting-a-network-interface-card.md) |



 

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

[IStats:: configurar](istats-configure.md)
</dt> <dt>

[IStats::D isconnect](istats-disconnect.md)
</dt> <dt>

[BLOBs de Monitor de Rede](network-monitor-blobs.md)
</dt> </dl>

 

 




