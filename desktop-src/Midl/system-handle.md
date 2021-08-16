---
title: atributo system_handle
description: O atributo \ system_handle\ especifica um tipo de identificador definido pelo sistema.
keywords:
- system_handle atributo MIDL
topic_type:
- apiref
api_name:
- system_handle
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 1cc89818db201f1aca84aa63c6aa49b6b7d9f80b7b6c5e211e724004606c653e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641262"
---
# <a name="system_handle-attribute"></a>atributo system_handle

O system_handle atributo especifica um tipo de identificador definido \[  \] pelo sistema que representa o acesso a um objeto do sistema.

``` syntax
[system_handle(system-handle-type[,optional-access-mask])]
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*system-handle-type* 
</dt> <dd>

Especifica uma das opções de tipo de identificador do sistema.

As opções válidas são:
* [sh_composition](sh-composition.md) - um alça de superfície DirectComposition
* [sh_event](sh-event.md) - um objeto de evento nomeado ou sem nome
* [sh_file](sh-file.md) - um arquivo ou dispositivo de E/S
* [sh_job](sh-job.md) - um objeto de trabalho
* [sh_mutex](sh-mutex.md) - um objeto mutex nomeado ou sem nome
* [sh_pipe](sh-pipe.md) - um objeto de pipe anônimo ou nomeado
* [sh_process](sh-process.md) - um objeto de processo
* [sh_reg_key](sh-reg-key.md) - uma chave do Registro
* [sh_section](sh-section.md) - uma seção de memória compartilhada
* [sh_semaphore](sh-semaphore.md) - um objeto de semáforo nomeado ou sem nome
* [sh_socket](sh-socket.md) - um objeto de soquete WinSock
* [sh_thread](sh-thread.md) - um objeto de thread
* [sh_token](sh-token.md) - um objeto de token de acesso

</dd> <dt>

*optional-access-mask*
</dt> <dd>

Opcionalmente, solicita direitos de acesso específicos aplicados ao alça duplicado. Por padrão, quando isso não for especificado, o handle será duplicado com o mesmo acesso. 

Para especificar um nível diferente de acesso, use direitos de acesso específicos do objeto correspondentes ao objeto do sistema subjacente selecionado.

Mais informações sobre como os direitos de acesso são propagados durante a duplicação podem ser encontradas na [documentação duplicateHandle.](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)

Links para listas de direitos de acesso para cada tipo de objeto podem ser encontrados na referência *DuplicateHandle,* bem como na página Ver também **os** títulos de cada `sh_*` parâmetro.

</dd> </dl>

## <a name="remarks"></a>Comentários

Para usar esse atributo, o `-target` sinalizador deve ser definido como `NT100` (ou superior) ao executar midl.exe.

Os alças do sistema são alças definidas pelo sistema operacional para fornecer acesso a um recurso do sistema. O tipo específico do objeto por trás do identificador deve ser especificado ao declarar o atributo.

Para um alça marcado como , o handle será duplicado no procedimento remoto e permanecerá válido durante `[in]` esse procedimento. No retorno do procedimento remoto, o alça duplicado é liberado. Para manter o acesso ao objeto subjacente, o aplicativo remoto deve duplicar o identificador em seu próprio espaço de endereço.

Por outro lado, para um alça marcado como , quando um procedimento remoto retorna um handle de uma chamada, o procedimento remoto perderá `[out]` a propriedade dele. Para manter o acesso ao objeto subjacente, o procedimento remoto deve duplicar o identificador e retornar a duplicata. O identificador retornado passa a ser de propriedade do chamador que assume a responsabilidade de fechar quando o acesso ao objeto do sistema subjacente não é mais necessário.

Como esse é um mecanismo para retransmitir o acesso a um objeto do sistema, esse atributo só é aplicável a chamadas entre procedimentos no mesmo computador.

Os parâmetros de criação e acesso dados ao objeto subjacente por trás do identificador do sistema em sua criação determinarão se ele pode ser realizado com êxito no contexto do procedimento remoto.

Uma matriz de pode ser passada para dentro ou para fora com a sintaxe encontrada na `system_handle` [**documentação size_is atributo.**](size-is.md)

## <a name="examples"></a>Exemplos

Os exemplos a seguir usam vários usos de `system_handle` . Para ver um exemplo completo, consulte o [exemplo SystemHandlePassing.](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SystemHandlePassing)

```c
interface MyInterface : IUnknown                         
{         
    HRESULT Proc1([in, system_handle(sh_file)] HANDLE writeThisFile);

    HRESULT Proc2([in, system_handle(sh_pipe, FILE_GENERIC_READ)] HANDLE readThisPipe);

    HRESULT Proc3([out, system_handle(sh_composition)] HANDLE* visual);

    HRESULT Proc4([in] DWORD cEvents, [out, system_handle(sh_event), size_is(cEvents)] HANDLE* pWatchAllTheseEvents);
}
```

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
|-|-|
| Cliente mínimo com suporte | Windows 10 Atualização de aniversário (versão 1607, build 14393) |
| Servidor mínimo com suporte | Windows Server 2016 (build 14393) |

## <a name="see-also"></a>Confira também

<dl> <dt>
<!--
[System Handle Passing sample code](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SystemHandlePassing)
</dt> <dt>
-->

[opção /target](./-target.md)
</dt> <dt>

[Associação e alças](../Rpc/binding-and-handles.md)
</dt> <dt>

[Alças e objetos](../sysinfo/handles-and-objects.md)
</dt> <dt>

[Arquivo IDL (definição de interface)](interface-definition-idl-file.md)
</dt> <dt>

[**Duplicatehandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)
</dt> <dt>

[Descritores de segurança](../secauthz/security-descriptors.md)
</dt></dl>
