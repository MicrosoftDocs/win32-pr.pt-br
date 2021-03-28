---
description: Essa classe é a classe pai para eventos de e/s de arquivo. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 8e006a63-a061-4b62-8f90-b8c8823bb047
title: Classe FileIo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2f7c032cb7af325efa1d2ea76702068fc7b3be62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967725"
---
# <a name="fileio-class"></a>Classe FileIo

Essa classe é a classe pai para eventos de e/s de arquivo.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Guid("{90cbdc39-4a3e-11d1-84f4-0000f80464e3}"), EventVersion(2)]
class FileIo : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Membros

A classe **FileIo** não define nenhum membro.

## <a name="remarks"></a>Comentários

Para habilitar os eventos de e/s de arquivo em uma sessão de log de kernel NT, especifique o sinalizador de **\_ \_ \_ \_ \_ e/s do arquivo de disco do sinalizador de rastreamento de eventos** no membro **EnableFlags** de uma estrutura de [**\_ \_ Propriedades de rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) ao chamar a função [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) Você também pode especificar um ou mais dos seguintes sinalizadores:

-   **\_ \_ \_ e/s do arquivo de sinalizador de rastreamento de eventos \_**
-   **\_inicialização de \_ es do arquivo de sinalizador de rastreamento de \_ \_ eventos \_**

Os consumidores de rastreamento de eventos podem implementar processamento especial para eventos de e/s de arquivo chamando a função [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e especificando [**FileIoGuid**](nt-kernel-logger-constants.md) como o parâmetro *pGuid* . Use os tipos de evento a seguir para identificar o evento real ao consumir eventos.



| Tipo de evento             | Descrição                                                                                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| O valor do tipo de evento é 0  | Evento de nome de arquivo. A classe do [**\_ nome do FileIo**](fileio-name.md) MOF define os dados do evento para esse evento.                                                                               |
| O valor do tipo de evento é 32 | Evento de criação de arquivo. A classe do [**\_ nome do FileIo**](fileio-name.md) MOF define os dados do evento para esse evento.                                                                             |
| O valor do tipo de evento é 35 | Evento de exclusão de arquivo. A classe do [**\_ nome do FileIo**](fileio-name.md) MOF define os dados do evento para esse evento.                                                                             |
| O valor do tipo de evento é 36 | Evento de encerramento do arquivo. Enumera todos os arquivos abertos no computador no final da sessão de rastreamento. A classe do [**\_ nome do FileIo**](fileio-name.md) MOF define os dados do evento para esse evento. |
| O valor do tipo de evento é 64 | Evento de criação de arquivo. A classe [**FileIo \_ Create**](fileio-create.md) MOF define os dados do evento para esse evento.                                                                         |
| O valor do tipo de evento é 72 | Evento de enumeração de diretório. A [**classe \_ DirEnum**](fileio-direnum.md) do do FileIo é que define os dados do evento para esse evento.                                                             |
| O valor do tipo de evento é 77 | Evento de notificação de diretório. A [**classe \_ DirEnum**](fileio-direnum.md) do do FileIo é que define os dados do evento para esse evento.                                                            |
| O valor do tipo de evento é 69 | Definir evento de informações. A classe do MOF [**\_ informações do FileIo**](fileio-info.md) define os dados do evento para esse evento.                                                                         |
| O valor do tipo de evento é 70 | Excluir evento de arquivo. A classe do MOF [**\_ informações do FileIo**](fileio-info.md) define os dados do evento para esse evento.                                                                             |
| O valor do tipo de evento é 71 | Renomear o evento de arquivo. A classe do MOF [**\_ informações do FileIo**](fileio-info.md) define os dados do evento para esse evento.                                                                             |
| O valor do tipo de evento é 74 | Evento de informações do arquivo de consulta. A classe do MOF [**\_ informações do FileIo**](fileio-info.md) define os dados do evento para esse evento.                                                                  |
| O valor do tipo de evento é 75 | Evento de controle do sistema de arquivos. A classe do MOF [**\_ informações do FileIo**](fileio-info.md) define os dados do evento para esse evento.                                                                     |
| O valor do tipo de evento é 76 | Fim do evento de operação. A classe MOF [**\_ aberta do FileIo**](fileio-opend.md) define os dados do evento para esse evento.                                                                      |
| O valor do tipo de evento é 67 | Evento de leitura de arquivo. A classe do MOF do [**FileIo \_ ReadWrite**](fileio-readwrite.md) define os dados do evento para esse evento.                                                                     |
| O valor do tipo de evento é 68 | Evento de gravação de arquivo. A classe do MOF do [**FileIo \_ ReadWrite**](fileio-readwrite.md) define os dados do evento para esse evento.                                                                    |
| O valor do tipo de evento é 65 | Evento de limpeza. O evento é gerado quando o último identificador do arquivo é liberado. A [**classe \_ SimpleOp**](fileio-simpleop.md) do do FileIo é que define os dados do evento para esse evento.   |
| O valor do tipo de evento é 66 | Fechar evento. O evento é gerado quando o objeto de arquivo é liberado. A [**classe \_ SimpleOp**](fileio-simpleop.md) do do FileIo é que define os dados do evento para esse evento.                     |
| O valor do tipo de evento é 73 | Evento de liberação. Esse evento é gerado quando os buffers de arquivo são totalmente liberados para o disco. A [**classe \_ SimpleOp**](fileio-simpleop.md) do do FileIo é que define os dados do evento para esse evento.  |



 

Os eventos de e/s de arquivo são registrados no início da operação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**\_V0 FileIo**](fileio-v0.md)
</dt> <dt>

[**FileIo \_ v1**](fileio-v1.md)
</dt> </dl>

 

 
