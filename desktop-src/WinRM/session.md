---
title: Objeto Session (WSManDisp. h)
description: Define as configurações de operações e de sessão.
ms.assetid: b98ca759-71cb-492e-8645-8766b202eb36
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows de objeto de sessão
- Gerenciamento Remoto do Windows de objeto de sessão, descrito
topic_type:
- apiref
api_name:
- Session
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2e47658ad8a89af5adb2135b86cc2ad9b6ef438
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919201"
---
# <a name="session-object-wsmandisph"></a>Objeto Session (WSManDisp. h)

Define as configurações de operações e de sessão. Todas as operações de Gerenciamento Remoto do Windows exigem a criação de uma **sessão** que se conecta a um computador remoto, BMC ( [*controlador de gerenciamento base*](windows-remote-management-glossary.md) ) ou o computador local. As operações de rede do WinRM incluem obter, gravar ou enumerar dados ou invocar métodos. Os métodos do objeto de **sessão** espelham as operações básicas definidas no protocolo WS-Management.

## <a name="members"></a>Membros

O objeto de **sessão** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto de **sessão** tem esses métodos.



| Método                                 | Descrição                                                                                                                 |
|:---------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**Criada**](session-create.md)       | Cria uma nova instância de um recurso e retorna o URI do novo objeto.<br/>                                      |
| [**Apagar**](session-delete.md)       | Exclui o recurso especificado no URI de recurso.<br/>                                                              |
| [**Enumerar**](session-enumerate.md) | Enumera um recurso de coleta, tabela ou log de mensagens.<br/>                                                         |
| [**Obter**](session-get.md)             | Recupera um recurso do serviço e retorna uma representação XML da instância atual do recurso.<br/> |
| [**Identificar**](session-identify.md)   | Consulta um computador remoto para determinar se ele dá suporte ao protocolo de WS-Management<br/>                                 |
| [**Chame**](session-invoke.md)       | Invoca um método que retorna os resultados da chamada de método.<br/>                                                    |
| [**Posicione**](session-put.md)             | Atualiza um recurso.<br/>                                                                                              |



 

### <a name="properties"></a>Propriedades

O objeto de **sessão** tem essas propriedades.



| Propriedade                                            | Tipo de acesso           | Descrição                                                                                                                                                                                                                 |
|:----------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BatchItems**](session-batchitems.md)<br/> | Leitura/gravação<br/> | Define e Obtém o número de itens em cada lote de enumeração. Esse valor não pode ser alterado durante uma enumeração. Por padrão, o padrão é um número ilimitado de itens. O provedor de recursos pode definir um limite.<br/> |
| [**Erro**](session-error.md)<br/>           | Somente leitura<br/>  | Obtém informações de erro adicionais em um fluxo XML.<br/>                                                                                                                                                              |
| [**Cedido**](session-timeout.md)<br/>       | Leitura/gravação<br/> | Define e obtém a quantidade máxima de tempo (em milissegundos) para o aplicativo cliente aguardar.<br/>                                                                                                                   |



 

## <a name="remarks"></a>Comentários

O objeto de **sessão** corresponde à interface [**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession) .

## <a name="examples"></a>Exemplos

O exemplo de código VBScript a seguir mostra como criar um objeto de **sessão** .


```VB
' Create a WSMan object.
Dim objWsman 
Set objWsman = CreateObject( "WSMAN.Automation" )

' Create Session object.
Dim objSession
Set objSession = objWsman.CreateSession
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                           |
| parâmetro<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[API de script do WinRM](winrm-scripting-api.md)
</dt> <dt>

[Sobre Gerenciamento Remoto do Windows](about-windows-remote-management.md)
</dt> <dt>

[Usando Gerenciamento Remoto do Windows](using-windows-remote-management.md)
</dt> <dt>

[Criando scripts no Gerenciamento Remoto do Windows](scripting-in-windows-remote-management.md)
</dt> <dt>

[Obtendo dados do computador local](obtaining-data-from-the-local-computer.md)
</dt> <dt>

[Obtendo dados de um computador remoto](obtaining-data-from-a-remote-computer.md)
</dt> </dl>

 

 





