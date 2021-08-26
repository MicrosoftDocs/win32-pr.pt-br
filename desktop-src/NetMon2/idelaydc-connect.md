---
description: o método Conexão conecta o NPP à rede usando uma placa de interface de rede especificada e fornece informações de configuração sobre a conexão.
ms.assetid: aae9ff9c-d077-4db2-a900-9916e4f7bb8b
title: 'método IDelaydC:: Conexão (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Connect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: e91db1dae0c67c5f35e46841867d3d3e15058cf0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477293"
---
# <a name="idelaydcconnect-method"></a>método IDelaydC:: Conexão

o método **Conexão** conecta o NPP à rede usando uma placa de interface de rede especificada e fornece informações de configuração sobre a conexão.

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

Identificador para o BLOB que especifica a NIC à qual você está se conectando e as informações de configuração sobre essa conexão.

</dd> <dt>

*StatusCallbackProc* \[ no\]
</dt> <dd>

Endereço da função de retorno de chamada do usuário, que é usada para receber atualizações de status, como gatilhos. Se nenhuma função de retorno de chamada for usada, defina esse parâmetro e o parâmetro *userContext* como **NULL**.

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

Se esse método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.

Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro (que incluem os erros retornados pela chamada interna **IDelaydC:: Configure** ):




| Código de retorno | Descrição | 
|-------------|-------------|
| <dl><dt><strong>NMERR_ALREADY_CONNECTED</strong></dt></dl> | Esta instância do objeto COM NPP já está conectada à rede.<br /> | 
| <dl><dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt></dl> | O BLOB de configuração está corrompido. Esse erro é gerado pela chamada <strong>IDelaydC:: Configure</strong> .<br /> | 
| <dl><dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt></dl> | O BLOB de entrada especificado por <em>hInputBlob</em> não tem uma entrada necessária para executar esta operação. esse erro pode ser gerado pela chamada <strong>IDelaydC:: Conexão</strong> ou <strong>IDelaydC:: Configure</strong> . Examine o BLOB de erro retornado por <em>hErrorBlob</em> para determinar qual entrada não foi encontrada.<br /> | 
| <dl><dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt></dl> | A função <strong>createBlob</strong> não foi chamada. Esse erro é gerado pela chamada <strong>IDelaydC:: Configure</strong> .<br /> | 
| <dl><dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt></dl> | A cadeia de caracteres não é terminada em nulo. Esse erro é gerado pela chamada <strong>IDelaydC:: Configure</strong> .<br /> | 
| <dl><dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt></dl> | A parte do gatilho do BLOB de entrada está corrompida. Esse erro é gerado pela chamada <strong>IDelaydC:: Configure</strong> .<br /> | 
| <dl><dt><strong>NMERR_INVALID_BLOB</strong></dt></dl> | O objeto especificado em <em>hInputBlob</em> não é um blob. Esse erro é gerado pela chamada <strong>IDelaydC:: Configure</strong> .<br /> | 
| <dl><dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt></dl> | O diretório de captura padrão não foi definido no registro. Use o caminho a seguir para definir o diretório de captura. <br /><pre class="syntax" data-space="preserve"><code>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\nm\Parameters\CapturePath</code></pre> | 
| <dl><dt><strong>NMERR_OUT_OF_MEMORY</strong></dt></dl> | Não havia memória disponível para executar esta operação. Esse erro é gerado pela chamada <strong>IDelaydC:: Configure</strong> .<br /> | 
| <dl><dt><strong>NMERR_TIMEOUT</strong></dt></dl> | O tempo limite da solicitação foi atingido. Esse erro é gerado pela chamada <strong>IDelaydC:: Configure</strong> .<br /> | 
| <dl><dt><strong>NMERR_UPLEVEL_BLOB</strong></dt></dl> | O número de versão do BLOB especificado em <em>hInputBlob</em> está incorreto. Esse erro é gerado pela chamada <strong>IDelaydC:: Configure</strong> .<br /> | 




 

## <a name="remarks"></a>Comentários

quando o método **Conexão** é chamado, o NPP chama automaticamente **IDelaydC:: Configure** usando o BLOB fornecido pelo *hInputBlob*. observe que todos os códigos de erro retornados pela chamada para **IDelaydC:: Configure** são passados de volta e retornados pela chamada **IDelaydC:: Conexão** .

Esse método deve ser chamado antes que você possa iniciar a captura de quadros. Observe que quando você se conecta à rede usando esse método, você deve continuar a usar os métodos de interface **IDelaydC** para capturar quadros.

O BLOB de entrada especificado pelo parâmetro *hInputBlob* pode ser obtido chamando **GetNPPBlobFromUI**, **GetNPPBlobTable** e **SelectNPPBlobFromTable**.

O BLOB de erro retornado em *hErrorBlob* contém informações de erro que o desenvolvedor ou o aplicativo pode usar para solução de problemas. O BLOB de erro retornado por *hErrorBlob* contém entradas que monitor de rede não pôde entender ou localizar no blob de entrada especificado em *hInputBlob*. Por exemplo, se \_ a entrada de blob NMERR não \_ \_ \_ \_ existir for retornada, a entrada monitor de rede não poderá localizar é incluída no blob de erros retornado.



| Para obter informações sobre                          | Consulte                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------|
| Obtendo o BLOB de entrada que representa uma NIC | [Selecionando uma placa de interface de rede](selecting-a-network-interface-card.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[IDelaydC:: configurar](idelaydc-configure.md)
</dt> <dt>

[IDelaydC::D isconnect](idelaydc-disconnect.md)
</dt> <dt>

[IDelaydC:: iniciar](idelaydc-start.md)
</dt> </dl>

 

 




