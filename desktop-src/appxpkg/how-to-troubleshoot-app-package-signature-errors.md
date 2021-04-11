---
title: Como solucionar problemas de erros de assinatura do pacote de aplicativo
description: Uma falha de implantação de aplicativo pode ser causada por uma falha ao validar a assinatura digital do pacote do aplicativo. Saiba como reconhecer essas falhas e o que fazer sobre elas.
ms.assetid: CE868296-87F6-4BD5-8AC5-914E429EDEBC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e0afe77ebfd478be5c652604ea575fc90b5d3ef
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104365825"
---
# <a name="how-to-troubleshoot-app-package-signature-errors"></a>Como solucionar problemas de erros de assinatura do pacote de aplicativo

Uma falha de implantação de aplicativo pode ser causada por uma falha ao validar a assinatura digital do pacote do aplicativo. Saiba como reconhecer essas falhas e o que fazer sobre elas.

Quando você implanta um aplicativo do Windows empacotado, o Windows sempre tenta validar a assinatura digital no pacote do aplicativo. Falhas durante a implantação do bloco de validação de assinatura do pacote. Mas o motivo pelo qual o pacote não foi validado pode não ser óbvio. Em particular, se você assinar seus pacotes com certificados privados para teste local, você geralmente também deve gerenciar a relação de confiança para esses certificados. Uma configuração de confiança de certificado incorreta pode levar a falhas de validação de assinatura.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Empacotamento, implantação e consulta de aplicativos do Windows](appx-portal.md)
-   [Verificação de confiança de certificado](/windows/desktop/SecCrypto/certificate-trust-verification)

### <a name="prerequisites"></a>Pré-requisitos

-   [Log de eventos do Windows](/windows/desktop/WES/windows-event-log) para diagnosticar falhas de instalação.
-   [Tarefas de certutil para gerenciar certificados](/previous-versions/orphan-topics/ws.10/cc772898(v=ws.10)) para manipulação de repositório de certificados durante a solução de problemas

## <a name="instructions"></a>Instruções

### <a name="step-1-examine-event-logs-for-diagnostic-information"></a>Etapa 1: examinar os logs de eventos para obter informações de diagnóstico

Dependendo de como você tentou implantar seu aplicativo, talvez você não tenha recebido um código de erro significativo para a falha de implantação. Nesse caso, geralmente você pode obter o código de erro diretamente dos logs de eventos.

**Para obter o código de erro dos logs de eventos**

1.  Execute **eventvwr. msc**.
2.  Vá para **Visualizador de eventos (local)**  >  **logs de aplicativos e serviços**  >  **Microsoft**  >  **Windows**.
3.  O primeiro log a ser verificado é **AppxPackagingOM**  >  **Microsoft-Windows-AppxPackaging/Operational**.
4.  Os erros relacionados à implantação são registrados em **AppXDeployment-Server**  >  **Microsoft-Windows-AppXDeploymentServer/Operational**.

    Para erros de implantação, procure o evento de erro mais recente 404. Esse evento de erro fornece o código de erro e uma descrição de por que a implantação falhou. Se um evento de erro 465 precede o evento 404, houve um problema ao abrir o pacote.

Se o erro 465 não ocorreu, consulte geral [solução de problemas de empacotamento, implantação e consulta de aplicativos do Windows](troubleshooting.md). Caso contrário, consulte esta tabela para obter códigos de erro comuns que podem aparecer na cadeia de caracteres de erro para o evento de erro 465:

| Código do erro | Erro                                 | Descrição                                                                                                          | Sugestão                                                                                                                                                                                                 |
|------------|---------------------------------------|----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x80073CF0 | ERRO \_ \_ ao instalar \_ pacote aberto \_ com falha | Não foi possível abrir o pacote do aplicativo.                                                                                 | Esse erro normalmente indica um problema com o pacote. Você precisa compilar e assinar o pacote novamente. Para obter mais informações, consulte [usando o app Packager](make-appx-package--makeappx-exe-.md). |
| 0x80080205 | APPX \_ E \_ \_ BLOCKMAP inválido            | O pacote do aplicativo foi adulterado ou tem um mapa de bloco inválido.                                                  | O pacote está corrompido. Você precisa compilar e assinar o pacote novamente. Para obter mais informações, consulte [usando o app Packager](make-appx-package--makeappx-exe-.md).                                  |
| 0x800B0004 | CONFIAR \_ E \_ assunto \_ não \_ confiável       | O pacote do aplicativo foi adulterado.                                                                              | O conteúdo do pacote não corresponde mais à sua assinatura digital. Você precisa assinar o pacote novamente. Para obter mais informações, consulte [como assinar um pacote de aplicativo usando Signtool](how-to-sign-a-package-using-signtool.md).  |
| 0x800B0100 | CONFIAR \_ E \_ noassinatura                 | O pacote do aplicativo não está assinado.                                                                                         | Somente pacotes de aplicativos Windows assinados podem ser implantados. Para obter informações sobre como assinar um pacote de aplicativo, consulte [como assinar um pacote de aplicativo usando Signtool](how-to-sign-a-package-using-signtool.md).                  |
| 0x800B0109 | raiz do certificado \_ E \_ não confiável \_              | A cadeia de certificados usada para assinar o pacote do aplicativo termina em um certificado raiz que não é confiável.           | Continue na etapa 2 para solucionar problemas de confiança do certificado.                                                                                                                                                  |
| 0x800B010A | encadeamento de CERT \_ E \_                     | Nenhuma cadeia de certificados pode ser compilada para uma autoridade raiz confiável do certificado que foi usado para assinar o pacote do aplicativo. | Continue na etapa 2 para solucionar problemas de confiança do certificado.                                                                                                                                                  |



 

### <a name="step-2-determine-the-certificate-chain-used-to-sign-the-app-package"></a>Etapa 2: determinar a cadeia de certificados usada para assinar o pacote do aplicativo

Para descobrir os certificados que o computador local deve confiar, você pode examinar a cadeia de certificados para a assinatura digital no pacote do aplicativo.

**Para determinar a cadeia de certificados**

1.  No explorador de arquivos, clique com o botão direito do mouse no pacote do aplicativo e selecione **Propriedades**.
2.  Na caixa de diálogo **Propriedades** , selecione a guia **assinaturas digitais** , que também exibe se a assinatura pode ser validada.
3.  Na lista assinatura, selecione a assinatura e clique no botão **detalhes** .
4.  Na caixa de diálogo **detalhes da assinatura digital** , clique no botão **Exibir certificado** .
5.  Na caixa de diálogo **certificado** , selecione a guia **caminho de certificação** .

O certificado principal na cadeia é o certificado raiz e o certificado inferior é o certificado de autenticação. Se apenas um único certificado estiver na cadeia, o certificado de autenticação também será seu próprio certificado raiz. Você pode determinar o número de série para cada certificado que você usa com o [certutil](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732443(v=ws.10)):

**Para determinar o número de série para cada certificado**

1.  No painel caminho de certificação, selecione o certificado e clique em **Exibir certificado**.
2.  Na caixa de diálogo certificado, selecione a guia **detalhes** , que exibe o número de série e outras propriedades úteis do certificado.

### <a name="step-3-determine-the-certificates-trusted-by-the-local-machine"></a>Etapa 3: determinar os certificados confiáveis pelo computador local

Para poder implantar um pacote de aplicativo, ele não deve ser confiável apenas no contexto do usuário, mas também no contexto do computador local. Como resultado, a assinatura digital pode aparecer válida quando exibida na guia assinaturas digitais da etapa anterior, mas ainda falha na validação durante a implantação do pacote do aplicativo.

**Para determinar se a cadeia de certificados usada para assinar o pacote do aplicativo é especificamente confiável pelo computador local**

1.  Execute este comando:

    ``` syntax
    CertUtil.exe -store Root rootCertSerialNumber
    ```

2.  Execute este comando:

    ``` syntax
    CertUtil.exe -store TrustedPeople signingCertSerialNumber
    ```

Se você não especificar o número de série do certificado, o [certutil](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732443(v=ws.10)) listará todos os certificados que são confiáveis para o computador local desse armazenamento.

O pacote pode falhar ao ser instalado devido a erros de encadeamento de certificados, mesmo que o certificado de autenticação não seja autoassinado e o certificado raiz esteja no repositório raiz do computador local. Nesse caso, pode haver um problema com a confiança para as autoridades de certificação intermediárias. Para obter mais informações sobre esse problema, consulte [trabalhando com certificados](/previous-versions/dotnet/netframework-3.0/ms731899(v=vs.85)).

## <a name="remarks"></a>Comentários

Se você determinou que o pacote não pôde ser implantado porque o certificado de autenticação não é confiável, não instale o pacote, a menos que você saiba onde ele foi originado e confie nele.

Se você quiser confiar manualmente no aplicativo para instalação (por exemplo, para instalar seu próprio pacote de aplicativo assinado por teste), você pode adicionar manualmente o certificado à relação de confiança de certificado do computador local no pacote do aplicativo.

**Para adicionar manualmente o certificado à relação de confiança de certificado do computador local**

1.  No explorador de arquivos, clique com o botão direito do mouse no pacote do aplicativo e, no menu de contexto pop-up, selecione **Propriedades**.
2.  Na caixa de diálogo **Propriedades** , selecione a guia **assinaturas digitais** .
3.  Na lista assinatura, selecione a assinatura e clique no botão **detalhes** .
4.  Na caixa de diálogo **detalhes da assinatura digital** , clique no botão **Exibir certificado** .
5.  Na caixa de diálogo **certificado** , clique no botão **Instalar certificado...** .
6.  No Assistente para importação de certificados, selecione **computador local** e clique em **Avançar**. Será necessário conceder privilégios de administrador para continuar.
7.  Selecione **Coloque todos os certificados no repositório a seguir** e navegue até o repositório de **pessoas confiáveis** .
8.  Clique em **Avançar** e em **concluir** para concluir o assistente.

Após essa adição manual, você pode ver que o certificado agora é confiável na caixa de diálogo de **certificado** .

Você pode remover o certificado depois de não precisar mais dele.

**Para remover o certificado**

1.  Execute **Cmd.exe** como administrador.
2.  No prompt de comando do administrador, execute este comando:

    ``` syntax
    Certutil -store TrustedPeople
    ```

3.  Procure o número de série do certificado que você instalou. Esse número é o *certid*.
4.  Execute este comando:

    ``` syntax
    Certutil -delStore TrustedPeople certID
    ```

Recomendamos que você evite adicionar manualmente certificados raiz ao [repositório de certificados de autoridades de certificação raiz confiáveis](/windows-hardware/drivers/install/trusted-root-certification-authorities-certificate-store)do computador local. Ter vários aplicativos assinados com certificados que se encadeam ao mesmo certificado raiz, como aplicativos de linha de negócios, pode ser mais eficiente do que instalar certificados individuais no repositório de pessoas confiáveis. O repositório de pessoas confiáveis contém certificados que são considerados confiáveis por padrão e, portanto, não são verificados por autoridades ou listas de certificados confiáveis ou cadeias superiores. Para obter considerações sobre como adicionar certificados ao repositório de certificados de autoridades de certificação raiz confiáveis, consulte [práticas recomendadas de assinatura de código](/previous-versions/windows/hardware/design/dn653556(v=vs.85)).

## <a name="security-considerations"></a>Considerações de segurança

Ao adicionar um certificado em [repositórios de certificados do computador local](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores), você afetará a confiança do certificado de todos os usuários no computador. Recomendamos que você instale todos os certificados de assinatura de código desejados para testar pacotes de aplicativos no repositório de certificados de pessoas confiáveis. Remova imediatamente esses certificados quando eles não forem mais necessários, para impedir que eles sejam usados para comprometer a confiança do sistema. Se você criar seus próprios certificados de teste para assinar pacotes de aplicativos, também recomendamos que você restrinja os privilégios associados ao certificado de teste. Para obter informações sobre como criar certificados de teste para assinar pacotes de aplicativos, consulte [como criar um certificado de assinatura de pacote de aplicativo](how-to-create-a-package-signing-certificate.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Amostras**
</dt> <dt>

[Criar amostra de pacote de aplicativo]https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingCreateAppx)
</dt> <dt>

**Conceitos**
</dt> <dt>

[Solucionar problemas de empacotamento, implantação e consulta de aplicativos Windows](troubleshooting.md)
</dt> <dt>

[Tarefas de certutil para gerenciar certificados](/previous-versions/orphan-topics/ws.10/cc772898(v=ws.10))
</dt> </dl>

 

 