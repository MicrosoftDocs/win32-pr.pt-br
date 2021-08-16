---
description: O Conexão conecta o NPP à rede usando uma NIC especificada e fornece informações de configuração sobre a conexão.
ms.assetid: 48189b2b-9889-4bd8-8972-26005fb7c341
title: Método I LTD::Conexão (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Connect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: f2095f25128e524b32b8ad8561ee85119537c32be5e61f77d5c72637396a2183
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118365604"
---
# <a name="iespconnect-method"></a>Método I LTD::Conexão

O **Conexão** conecta o NPP à rede usando uma NIC especificada e fornece informações de configuração sobre a conexão.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT STDMETHODCALLTYPE Connect(
  [in]  HBLOB hInputBlob,
  [in]  DWORD StatusCallbackProc,
  [in]  DWORD UserContext,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hInputBlob* \[ Em\]
</dt> <dd>

Lidar com o BLOB que especifica a NIC à que o NPP se conecta e as informações de configuração para essa conexão.

</dd> <dt>

*StatusCallbackProc* \[ Em\]
</dt> <dd>

Endereço da função de retorno de chamada do usuário, que recebe atualizações de status, como gatilhos. Se uma função de retorno de chamada não for usada, de definir esse parâmetro e o *parâmetro UserContext* como **NULL.**

</dd> <dt>

*UserContext* \[ Em\]
</dt> <dd>

Valor passado quando a função de retorno de chamada do usuário é chamada. O valor desse parâmetro normalmente é HWND ou um ponteiro 'this'. Se uma função de retorno de chamada não for especificada, de definir esse parâmetro e o *parâmetro StatusCallbackProc* como **NULL.**

</dd> <dt>

*hErrorBlob* \[ out\]
</dt> <dd>

Tratar para um BLOB de erro que contém informações de erro adicionais.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, o valor de retorno será NMERR \_ SUCCESS.

Se o método não for bem-sucedido, o valor retornado será um dos seguintes códigos de erro (que incluem os erros retornados pela chamada **interna I CODES::Configure):**



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Código de retorno</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt><strong>NMERR_ALREADY_CONNECTED</strong></dt> </dl></td>
<td>Essa instância do objeto COM do NPP já está conectada à rede.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt> </dl></td>
<td>O BLOB de configuração está corrompido. Esse erro é gerado pela <strong>chamada I LTD::Configure.</strong><br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt> </dl></td>
<td>O BLOB de entrada especificado pelo parâmetro <em>hInputBlob</em> não tem uma entrada necessária para executar essa operação. Esse erro pode ser gerado pela chamada <strong>I LTD::Conexão</strong> <strong>ou I LTD::Configure.</strong> Veja o erro BLOB retornado por <em>hErrorBlob</em> para determinar qual entrada não foi encontrada.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt> </dl></td>
<td>A <strong>função CreateBlob</strong> não foi chamada. Esse erro é gerado pela <strong>chamada I LTD::Configure.</strong><br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt> </dl></td>
<td>A cadeia de caracteres não é terminada em nulo. Esse erro é gerado pela <strong>chamada I LTD::Configure.</strong><br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt> </dl></td>
<td>A parte do gatilho do BLOB de entrada está corrompida. Esse erro é gerado pela <strong>chamada I LTD::Configure.</strong><br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_INVALID_BLOB</strong></dt> </dl></td>
<td>O objeto especificado em <em>hInputBlob</em> não é um BLOB. Esse erro é gerado pela <strong>chamada I LTD::Configure.</strong><br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt> </dl></td>
<td>O diretório de captura padrão não foi definido no Registro. Use o caminho a seguir para definir o diretório de captura. <br/>
<pre class="syntax" data-space="preserve"><code>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\nm\Parameters\CapturePath</code></pre></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_OUT_OF_MEMORY</strong></dt> </dl></td>
<td>A memória necessária para executar essa operação não está disponível. Esse erro é gerado pela <strong>chamada I LTD::Configure.</strong><br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>NMERR_TIMEOUT</strong></dt> </dl></td>
<td>A solicitação passou do tempo. Esse erro é gerado pela <strong>chamada I LTD::Configure.</strong><br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_UPLEVEL_BLOB</strong></dt> </dl></td>
<td>O número de versão do BLOB especificado em <em>hInputBlob</em> está incorreto. Esse erro é gerado pela <strong>chamada I LTD::Configure.</strong><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Comentários

Quando o **Conexão** é chamado, Monitor de Rede chama automaticamente **I LTD::Configure** usando o BLOB fornecido pelo *parâmetro hInputBlob.* Observe que todos os códigos de erro retornados pela chamada para **I LTD::Configure** são passados de volta e retornados pela chamada **I LTD::Conexão.**

Esse método deve ser chamado antes que você possa iniciar a captura de quadros. Observe que, ao se conectar à rede usando esse método, você deve continuar a usar a interface **I TWITTER** para capturar quadros.

O BLOB de entrada especificado por *hInputBlob* pode ser obtido chamando **GetNPPBlobFromUI**, **GetNPPBlobTable** e **SelectNPPBlobFromTable**.

O BLOB de erro retornado por *hErrorBlob* contém entradas que Monitor de Rede não foi possível entender ou encontrar no BLOB de entrada especificado em *hInputBlob*. O BLOB de erro retornado contém informações de erro que o aplicativo pode usar para solução de problemas. Por exemplo, se A ENTRADA DE BLOB NMERR NÃO EXISTIR for retornada, a entrada que Monitor de Rede não foi possível encontrar será incluída no BLOB de erro \_ \_ \_ \_ \_ retornado.



| Para obter informações sobre                          | Consulte                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------|
| Obtendo o BLOB de entrada que representa uma NIC | [Selecionando uma placa de interface de rede](selecting-a-network-interface-card.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[I LTDA](iesp.md)
</dt> <dt>

[IRIA::Configure](iesp-configure.md)
</dt> <dt>

[I LTD::D conectar](iesp-disconnect.md)
</dt> <dt>

[I LTD::Start](iesp-start.md)
</dt> </dl>

 

 




