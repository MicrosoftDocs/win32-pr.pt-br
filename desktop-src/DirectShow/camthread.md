---
description: A classe CAMThread é uma classe abstrata para gerenciar threads de trabalho.
ms.assetid: c217d879-0203-4566-96ad-7463b05bc990
title: Classe CAMThread (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e5c2bde058267ae4c530f33a96778792d5fe247b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757048"
---
# <a name="camthread-class"></a>Classe CAMThread

A `CAMThread` classe é uma classe abstrata para gerenciar threads de trabalho.



| Variáveis de membro protegido                                 | Descrição                                                                  |
|------------------------------------------------------------|------------------------------------------------------------------------------|
| [**\_hThread m**](camthread-m-hthread.md)                  | Identificador para o thread.                                                        |
| Variáveis de membro público                                    | Descrição                                                                  |
| [**\_AccessLock m**](camthread-m-accesslock.md)            | Seção crítica que impede que o thread seja acessado por outros threads. |
| [**\_WorkerLock m**](camthread-m-workerlock.md)            | Seção crítica que bloqueia os dados compartilhados entre threads.                       |
| Métodos públicos                                             | Descrição                                                                  |
| [**CAMThread**](camthread-camthread.md)                   | Método de construtor.                                                          |
| [**~ CAMThread**](camthread--camthread.md)                | Método destruidor. VirtuaisLUNs.                                                  |
| [**InitialThreadProc**](camthread-initialthreadproc.md)   | Chama o método ThreadProc quando o thread é criado.                      |
| [**Criar**](camthread-create.md)                         | Cria o thread.                                                          |
| [**CallWorker**](camthread-callworker.md)                 | Sinaliza o thread com uma solicitação.                                           |
| [**Fechar**](camthread-close.md)                           | Aguarda até que o thread saia e, em seguida, libera seus recursos.                   |
| [**ThreadExists**](camthread-threadexists.md)             | Consulta se o thread existe.                                           |
| [**GetRequest**](camthread-getrequest.md)                 | Aguarda a próxima solicitação.                                                  |
| [**CheckRequest**](camthread-checkrequest.md)             | Verifica se há uma solicitação, sem bloqueio.                              |
| [**Responder**](camthread-reply.md)                           | Responde a uma solicitação.                                                        |
| [**GetRequestHandle**](camthread-getrequesthandle.md)     | Recupera um identificador para o evento sinalizado pelo método CallWorker.           |
| [**GetRequestParam**](camthread-getrequestparam.md)       | Recupera a solicitação mais recente.                                                |
| [**CoInitializeHelper**](camthread-coinitializehelper.md) | Chama CoInitializeEx no início do thread.                             |
| Métodos virtuais puros                                       | Descrição                                                                  |
| [**ThreadProc**](camthread-threadproc.md)                 | Procedimento de thread.                                                            |



 

## <a name="remarks"></a>Comentários

Essa classe fornece métodos para criar um thread de trabalho, passar solicitações para o thread e aguardar a saída do thread. Para usar essa classe, faça o seguinte:

-   Derive uma classe de `CAMThread` e substitua o método virtual puro [**CAMThread:: ThreadProc**](camthread-threadproc.md). Esse método é o procedimento de thread que é chamado no início do thread.
-   Em seu aplicativo, crie uma instância da classe derivada. A criação do objeto não cria o thread. Para criar o thread, chame o método [**CAMThread:: Create**](camthread-create.md) .
-   Para enviar solicitações para o thread, chame o método [**CAMThread:: CallWorker**](camthread-callworker.md) . Esse método usa um parâmetro DWORD, cujo significado é definido por sua classe. O método é bloqueado até que o thread responda (veja abaixo).
-   Em seu procedimento de thread, responda a solicitações chamando [**CAMThread:: GetRequest**](camthread-getrequest.md) ou [**CAMThread:: CheckRequest**](camthread-checkrequest.md). O método GetRequest é bloqueado até que outro thread chame CallWorker. O método CheckRequest é sem bloqueio, o que permite que o thread Verifique se há novas solicitações enquanto trabalha de forma assíncrona.
-   Quando o thread recebe uma solicitação, chame [**CAMThread:: Reply**](camthread-reply.md) para desbloquear o thread de chamada. O método Reply usa um parâmetro DWORD, que é passado para o thread de chamada como o valor de retorno para CallWorker.

Quando terminar com o thread, chame o método [**CAMThread:: Close**](camthread-close.md) . Esse método aguarda a saída do thread e fecha o identificador de thread. Sua mensagem ThreadProc deve ser garantida para sair, seja por conta própria ou em resposta a uma solicitação CallWorker. O método destruidor também chama Close.

O exemplo a seguir ilustra estas etapas:


```C++
class MyThread : public CAMThread
{
protected:
    DWORD ThreadProc(void);
};

DWORD MyThread::ThreadProc()
{
    BOOL bShutDown = FALSE;
    while (!bShutDown)
    {
        DWORD req = GetRequest();
        printf("Request: %d\n", req);
        bShutDown = (req == 0);
        Reply(bShutDown ? S_FALSE : S_OK);
    }
    printf("Quitting Thread\n");
    return 1;
}

void main()
{
    MyThread thread;
    DWORD reply;
    
    thread.Create();
    reply = thread.CallWorker(3);
    reply = thread.CallWorker(0); // Thread exits.
}
```



Em sua classe derivada, você também pode definir funções de membro que validam os parâmetros para CallWorker. O exemplo a seguir mostra uma maneira típica de fazer isso:


```C++
enum Command {CMD_INIT, CMD_RUN, CMD_STOP, CMD_EXIT};

HRESULT Init(void)  { return CallWorker(CMD_INIT); }
HRESULT Run(void)   { return CallWorker(CMD_RUN); }
HRESULT Stop(void)  { return CallWorker(CMD_STOP); }
HRESULT Exit(void)  { return CallWorker(CMD_EXIT); }
```



A `CAMThread` classe fornece duas seções críticas como variáveis de membro público. Use `CAMThread::m_AccessLock` para bloquear o acesso do thread por outros threads. (Por exemplo, os métodos Create e CallWorker mantêm esse bloqueio para serializar operações no thread.) Use [**CAMThread:: m \_ WorkerLock**](camthread-m-workerlock.md) para bloquear dados compartilhados entre threads.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




