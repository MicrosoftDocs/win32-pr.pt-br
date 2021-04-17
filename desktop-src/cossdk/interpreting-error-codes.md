---
description: Interpretando códigos de erro
ms.assetid: df2fe03b-2f5f-4958-926f-17e3a025a9b5
title: Interpretando códigos de erro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 659ee7def9feff50d375a07ab201e1cca25bffd7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787569"
---
# <a name="interpreting-error-codes"></a>Interpretando códigos de erro

Depois de determinar qual aplicativo é a origem de um problema, você precisa descobrir qual erro ocorreu. Os erros são gerados e relatados em formatos diferentes, dependendo do idioma usado pelo aplicativo.

Nos valores de Microsoft Visual C++, êxito, aviso e falha são retornados usando um número de 32 bits conhecido como **HRESULT**. Para obter uma lista de valores de **HRESULT** definidos pelo sistema, consulte o arquivo de cabeçalho Winerror. h incluído com o SDK do Windows. Esse arquivo inclui todos os códigos de erro COM+ e descrições. Para obter mais informações sobre valores **HRESULT** , consulte [tratamento de erros](/windows/desktop/com/error-handling-in-com).

Na linguagem Java, uma instância de com. ms. com. comfailbackexception é gerada para indicar falha, em que o objeto ComFailException especifica um **HRESULT**. Uma instância de com. ms. com. comsuccessfulexception indica êxito com um valor de retorno de false. Para obter informações sobre como interpretar essas exceções, consulte a documentação do Microsoft Visual J++.

> [!Note]  
> Os processos do servidor de aplicativos COM+ que hospedam objetos do Visual J++ não ficarão ociosos (mesmo com zero objetos ativos), a menos que você desative a depuração JIT no IDE do VJ6. Para obter informações sobre como fazer isso, consulte a documentação do Visual J++.

 

No Visual Basic, você pode recuperar valores **HRESULT** examinando a propriedade Err. Number. Uma descrição do erro pode ser recuperada com a propriedade Err. Description.

Você também pode usar o utilitário ERRLOOK no Microsoft Visual Studio para recuperar uma mensagem de erro do sistema ou uma mensagens de erro do módulo. ERRLOOK recuperará automaticamente o texto da mensagem de erro se você arrastar e soltar um valor hexadecimal ou decimal do depurador do Visual Studio ou de outro aplicativo habilitado para automação. Você também pode inserir um valor digitando-o ou colando-o na área de transferência do IDE e clicando na opção **Pesquisar** .

O método C++ a seguir imprime uma descrição do erro, com base na entrada **HRESULT**.


```C++
#include <stdio.h>
#include <windows.h>
#include <tchar.h>

void ErrorDescription(HRESULT hr) 
{ 
     if(FACILITY_WINDOWS == HRESULT_FACILITY(hr)) 
         hr = HRESULT_CODE(hr); 
     TCHAR* szErrMsg; 

     if(FormatMessage( 
       FORMAT_MESSAGE_ALLOCATE_BUFFER|FORMAT_MESSAGE_FROM_SYSTEM, 
       NULL, hr, MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT), 
       (LPTSTR)&szErrMsg, 0, NULL) != 0) 
     { 
         _tprintf(TEXT("%s"), szErrMsg); 
         LocalFree(szErrMsg); 
     } else 
         _tprintf( TEXT("[Could not find a description for error # %#x.]\n"), hr); 
}
```



A tabela a seguir fornece descrições de códigos de erro comuns no COM+.



| Códigos do Erro                                                   | Definições                                                                                                                                                                                                      |
|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| COMAdmin \_ E \_ ALREADYINSTALLED<br/>                      | O objeto já está registrado.<br/>                                                                                                                                                                     |
| COMAdmin \_ E \_ arquivo de aplicativo \_ \_ READFAIL<br/>                   | Erro ao ler o arquivo de aplicativo.<br/>                                                                                                                                                          |
| versão do \_ \_ arquivo de \_ aplicativo \_ COMAdmin E<br/>                    | Número de versão inválido no arquivo de aplicativo.<br/>                                                                                                                                                           |
| COMAdmin \_ E \_ arquivo de aplicativo \_ \_ WRITEFAIL<br/>                  | Erro ao gravar no arquivo de aplicativo.<br/>                                                                                                                                                       |
| COMAdmin \_ E \_ APPDIRNOTFOUND<br/>                        | O diretório de instalação do aplicativo não foi encontrado.<br/>                                                                                                                                                          |
| \_aplicativo COMQC \_ E \_ não \_ na fila<br/>                 | Somente aplicativos COM+ marcados como "enfileirados" podem ser criados usando o moniker "fila".<br/>                                                                                                                      |
| COMAdmin \_ E \_ APPLICATIONEXISTS<br/>                     | O aplicativo já está instalado.<br/>                                                                                                                                                                 |
| COMAdmin \_ E \_ aplicado \_ corresponde a \_ CLSID<br/>                | Um CLSID com o mesmo GUID que a nova ID de aplicativo já está instalado neste computador.<br/>                                                                                                            |
| o aplicativo COMAdmin \_ E \_ \_ não \_ está em execução<br/>                     | O aplicativo especificado não está em execução no momento.<br/>                                                                                                                                                   |
| COMAdmin \_ E \_ AUTHENTICATIONLEVEL<br/>                   | Não é possível definir o nível de autenticação necessário para a solicitação de atualização.<br/>                                                                                                                                       |
| COMAdmin \_ E \_ BADPATH<br/>                               | O caminho do arquivo é inválido.<br/>                                                                                                                                                                             |
| COMAdmin \_ E \_ BADREGISTRYLIBID<br/>                      | A ID da biblioteca de tipos registrada é inválida.<br/>                                                                                                                                                            |
| COMAdmin \_ E \_ BADREGISTRYPROGID<br/>                     | O ProgID do componente está ausente ou corrompido.<br/>                                                                                                                                                         |
| COMAdmin \_ E \_ não é possível \_ \_ exportar o \_ proxy de aplicativo \_<br/>          | O proxy de aplicativo não é exportável.<br/>                                                                                                                                                              |
| COMAdmin \_ E \_ \_ não pode \_ iniciar o \_ aplicativo<br/>                  | Falha ao iniciar o aplicativo porque ele é um aplicativo de biblioteca ou um proxy de aplicativo.<br/>                                                                                                       |
| COMAdmin \_ E \_ não é possível \_ \_ exportar o \_ \_ aplicativo sys<br/>            | O aplicativo do sistema não é exportável.<br/>                                                                                                                                                             |
| COMAdmin \_ E \_ não \_ assinar \_ o \_ componente<br/>        | O usuário não pode assinar este componente porque o componente pode ter sido importado.<br/>                                                                                                             |
| COMAdmin \_ E \_ CANTCOPYFILE<br/>                          | Ocorreu um erro ao copiar o arquivo.<br/>                                                                                                                                                                   |
| COMAdmin \_ E \_ CLSIDORIIDMISMATCH<br/>                    | Os CLSIDs ou IIDs do arquivo de aplicativo não correspondem às DLLs correspondentes.<br/>                                                                                                                                      |
| DEST- \_ \_ destino de \_ movimentação de comp \_ - \_ admin<br/>                 | A movimentação do componente falhou porque o aplicativo de destino não existe mais.<br/>                                                                                                                       |
| transferência do COMAdmin \_ E \_ comp \_ \_ bloqueada<br/>                    | A movimentação do componente não foi permitida porque o aplicativo de origem ou de destino é um aplicativo de sistema ou está atualmente bloqueado contra alterações.<br/>                                                |
| COMAdmin \_ E \_ compfile \_ BADTLB<br/>                      | Não foi possível carregar a biblioteca de tipos.<br/>                                                                                                                                                                 |
| COMAdmin \_ E \_ compfile \_ CLASSNOTAVAIL<br/>               | A DLL não oferece suporte aos componentes listados na biblioteca de tipos.<br/>                                                                                                                                   |
| COMAdmin \_ E \_ compfile \_ DOESNOTEXIST<br/>                | Este arquivo não existe.<br/>                                                                                                                                                                             |
| COMAdmin \_ E \_ compfile \_ GETCLASSOBJ<br/>                 | O método [**GetClassObject**](/windows/desktop/api/objidl/nf-objidl-iclassactivator-getclassobject) falhou na dll.<br/>                                                                                                                |
| COMAdmin \_ E \_ compfile \_ LOADDLLFAIL<br/>                 | Não foi possível carregar a DLL.<br/>                                                                                                                                                                          |
| COMAdmin \_ E \_ compfile \_ noregistrador<br/>                 | O registrador de componentes referenciado neste arquivo não está disponível.<br/>                                                                                                                                     |
| COMAdmin \_ E \_ compfile não \_ instalável<br/>              | O arquivo não contém componentes ou informações de componente.<br/>                                                                                                                                        |
| COMAdmin \_ E \_ COREQCOMPINSTALLED<br/>                    | Um componente no mesmo DLL já está instalado.<br/>                                                                                                                                                     |
| COMAdmin \_ E \_ DLLLOADFAILED<br/>                         | Não foi possível carregar a DLL.<br/>                                                                                                                                                                          |
| COMAdmin \_ E \_ DLLREGISTERSERVER<br/>                     | A função [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) falhou quando o componente foi instalado.<br/>                                                                                                  |
| COMAdmin \_ E \_ EVENTCLASS \_ \_ não é \_ assinante<br/>      | Uma classe de evento não pode ser configurada como um componente de assinante. Quando é feita uma tentativa de criar uma assinatura com uma classe de evento como assinante, esse erro é retornado.<br/>                          |
| COMAdmin \_ E \_ INVALIDUSERIDS<br/>                        | Um ou mais usuários no arquivo de aplicativo não são válidos.<br/>                                                                                                                                              |
| COMAdmin \_ E \_ envio de submissões<br/>                            | O objeto não foi encontrado no catálogo.<br/>                                                                                                                                                              |
| PROXY de aplicativo do COMAdmin \_ E \_ lib \_ \_ \_ incompatível<br/>         | Aplicativos de biblioteca e proxies de aplicativo são incompatíveis. Esse erro é retornado quando é feita uma tentativa de exportar um proxy de aplicativo e a propriedade de ativação do aplicativo é uma biblioteca. <br/> |
| COMAdmin \_ E \_ NOREGISTRYCLSID<br/>                       | O CLSID do componente está ausente ou corrompido.<br/>                                                                                                                                                          |
| COMAdmin \_ E \_ NOSERVERSHARE<br/>                         | Nenhum compartilhamento de arquivo de servidor está disponível.<br/>                                                                                                                                                                    |
| COMAdmin \_ E não \_ alterável<br/>                         | As alterações neste objeto e em seus subobjetos foram desabilitadas.<br/>                                                                                                                                        |
| COMAdmin \_ E não \_ excluível<br/>                         | A função de exclusão foi desabilitada para este objeto.<br/>                                                                                                                                                |
| COMAdmin \_ E \_ NOTINREGISTRY<br/>                         | O objeto não foi encontrado no registro.<br/>                                                                                                                                                                     |
| COMAdmin \_ E \_ Nouser<br/>                                | Um ou mais usuários não são válidos.<br/>                                                                                                                                                                      |
| \_o objeto COMAdmin E \_ \_ \_ não \_ existe<br/>              | Um dos objetos especificados não pode ser encontrado.<br/>                                                                                                                                                         |
| pai de COMAdmin \_ E \_ objeto \_ \_ ausente<br/>               | Um dos objetos inseridos ou atualizados não pertence a uma coleção pai válida.<br/>                                                                                                            |
| COMAdmin \_ E \_ objecterrors<br/>                          | Ocorreram erros ao acessar um ou mais objetos. Para obter mais informações, consulte a coleção [**errorInfo**](errorinfo.md) .<br/>                                                                               |
| COMAdmin \_ E \_ objectexistentes<br/>                          | O objeto que você está tentando adicionar ou renomear já existe.<br/>                                                                                                                                        |
| COMAdmin \_ E \_ objectinválido<br/>                         | Uma ou mais das propriedades do objeto estão ausentes ou são inválidas.<br/>                                                                                                                                        |
| COMAdmin \_ E \_ OBJECTNOTPOOLABLE<br/>                     | Este objeto não pode ser colocado em pool.<br/>                                                                                                                                                                      |
| COMAdmin \_ E \_ PROPERTYSAVEFAILED<br/>                    | Uma ou mais configurações de propriedade são inválidas ou estão em conflito entre si.<br/>                                                                                                                      |
| estouro de \_ Propriedade E COMadmin \_ \_<br/>                    | O valor da propriedade é muito grande.<br/>                                                                                                                                                                      |
| COMAdmin \_ E \_ REGFILE \_ corrompidos<br/>                      | O arquivo de registro está corrompido.<br/>                                                                                                                                                                     |
| COMAdmin \_ E \_ REGISTERTLB<br/>                           | O sistema não pôde registrar a biblioteca de tipos.<br/>                                                                                                                                                   |
| COMAdmin \_ E \_ REGISTRARFAILED<br/>                       | Ocorreram erros durante o registrador de componentes.<br/>                                                                                                                                                     |
| COMAdmin \_ E \_ REMOTEINTERFACE<br/>                       | As informações da interface estão ausentes ou foram alteradas.<br/>                                                                                                                                                   |
| COMAdmin \_ E \_ requer \_ \_ plataforma diferente<br/>         | Esta operação não está habilitada nesta plataforma.<br/>                                                                                                                                                       |
| a função COMAdmin \_ E \_ \_ \_ não \_ existe<br/>                | Uma função atribuída a um componente, interface ou método não existe no aplicativo.<br/>                                                                                                               |
| COMAdmin \_ E \_ ROLEEXISTS<br/>                            | A função já existe.<br/>                                                                                                                                                                              |
| COMAdmin \_ E \_ SERVICENOTINSTALLED<br/>                   | O serviço não está instalado.<br/>                                                                                                                                                                         |
| sessão do COMAdmin \_ E \_<br/>                               | Não há suporte para a versão do catálogo do servidor.<br/>                                                                                                                                                          |
| COMAdmin \_ S \_ SOMEALREADYPAUSED<br/>                     | Um ou mais dos processos de aplicativos especificados já foram pausados.<br/>                                                                                                                               |
| COMAdmin \_ S \_ SOMEALREADYRUNNING<br/>                    | Um ou mais dos processos de aplicativos especificados já estavam em execução.<br/>                                                                                                                              |
| COMAdmin \_ E \_ Iniciar \_ aplicativo \_ precisa de \_ componentes<br/>         | Para iniciar o aplicativo, você deve ter componentes em um aplicativo.<br/>                                                                                                                                 |
| COMAdmin \_ E \_ SVCAPP \_ não \_ poolable \_ ou \_ recicláveis<br/> | Os aplicativos COM+ em execução como um serviço NT não podem ser marcados como em pool ou reciclados.<br/>                                                                                                               |
| COMAdmin \_ E \_ SYSTEMAPP<br/>                             | Esta operação não pode ser executada no aplicativo do sistema.<br/>                                                                                                                                         |
| COMAdmin \_ E \_ usuário \_ no \_ conjunto<br/>                         | Um ou mais usuários já estão atribuídos a um conjunto de partições local.<br/>                                                                                                                                      |
| COMAdmin \_ E \_ USERPASSWDNOTVALID<br/>                    | A identidade ou a senha definida no aplicativo não é válida.<br/>                                                                                                                                         |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Política de FailFast e isolamento de falhas](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[Localizando a origem de um erro](finding-the-source-of-an-error.md)
</dt> <dt>

[Como o COM+ modifica valores de retorno](how-com--modifies-return-values.md)
</dt> <dt>

[Estratégias para lidar com erros no COM+](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[Solução de problemas](troubleshooting-the-com--crm.md)
</dt> </dl>

 

