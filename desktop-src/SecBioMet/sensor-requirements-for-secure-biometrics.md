---
title: Requisitos de sensor para biometria segura
description: Requisitos de sensor para biometria segura
ms.assetid: 6D5709E9-7B6B-4D6C-BF85-C6FB5DF5A7EE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82f4e41f8300a124115c2b6cd380f904f216f491
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105810523"
---
# <a name="sensor-requirements-for-secure-biometrics"></a><span data-ttu-id="c4286-103">Requisitos de sensor para biometria segura</span><span class="sxs-lookup"><span data-stu-id="c4286-103">Sensor requirements for secure biometrics</span></span>

<span data-ttu-id="c4286-104">A Microsoft aproveita Trusted Platform Module (TPM) 2,0 para garantir que, no hardware apropriado, o software (até e incluindo o malware no nível do kernel) não possa produzir uma autenticação biométrica válida se a biométrica do usuário não tiver sido fornecida no momento da autenticação.</span><span class="sxs-lookup"><span data-stu-id="c4286-104">Microsoft leverages Trusted Platform Module (TPM) 2.0 to ensure that on appropriate hardware, software (up to and including kernel-level malware) cannot produce a valid biometric authentication if the user’s biometric was not provided at the time of authentication.</span></span>

<span data-ttu-id="c4286-105">Para fazer isso, usamos autorizações baseadas em sessão do TPM 2,0 e o sensor que executa a extração de recursos e a correspondência em um ambiente de execução confiável.</span><span class="sxs-lookup"><span data-stu-id="c4286-105">To do this, we use TPM 2.0 session-based authorizations and the sensor performing feature extraction and matching in a trusted execution environment.</span></span> <span data-ttu-id="c4286-106">Na primeira vez que o Windows Biometric Framework vê um sensor seguro (conforme relatado pelo recurso de sensor seguro), ele provisiona um segredo que é compartilhado entre o sensor biométrico seguro e o TPM.</span><span class="sxs-lookup"><span data-stu-id="c4286-106">The first time the Windows Biometric Framework sees a secure sensor (as reported by the secure sensor capability), it provisions a secret that is shared between the secure biometric sensor and the TPM.</span></span> <span data-ttu-id="c4286-107">Esse segredo nunca é novamente exposto ao sistema operacional e é exclusivo para cada sensor.</span><span class="sxs-lookup"><span data-stu-id="c4286-107">That secret is never again exposed to the OS, and it is unique to each sensor.</span></span>

<span data-ttu-id="c4286-108">Para executar uma autenticação, a Windows Biometric Framework abre uma sessão com o TPM e Obtém um nonce.</span><span class="sxs-lookup"><span data-stu-id="c4286-108">To perform an authentication, the Windows Biometric Framework opens a session with the TPM and obtains a nonce.</span></span> <span data-ttu-id="c4286-109">O nonce é passado para o sensor seguro como parte de uma operação de correspondência segura.</span><span class="sxs-lookup"><span data-stu-id="c4286-109">The nonce is passed into the secure sensor as part of a secure match operation.</span></span> <span data-ttu-id="c4286-110">O sensor executa a correspondência no ambiente de execução confiável e, se for bem-sucedido, calcula um HMAC sobre esse nonce e a identidade do usuário que foi identificado.</span><span class="sxs-lookup"><span data-stu-id="c4286-110">The sensor performs the match in the trusted execution environment, and if it is successful, calculates an HMAC over that nonce and the identity of the user who was identified.</span></span>

<span data-ttu-id="c4286-111">Esse HMAC pode ser usado pelo Windows Biometric Framework para executar operações criptográficas no TPM para o usuário que foi identificado.</span><span class="sxs-lookup"><span data-stu-id="c4286-111">This HMAC can be used by the Windows Biometric Framework to perform cryptographic operations in the TPM for the user who was identified.</span></span> <span data-ttu-id="c4286-112">O HMAC é de curta duração e expira após alguns segundos.</span><span class="sxs-lookup"><span data-stu-id="c4286-112">The HMAC is short-lived, and expires after a few seconds.</span></span>

<span data-ttu-id="c4286-113">Usando esse protocolo, após o provisionamento inicial, não há dados confidenciais contidos no sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="c4286-113">Using this protocol, after the initial provisioning, no sensitive data is contained in the OS.</span></span> <span data-ttu-id="c4286-114">Os segredos são mantidos pelo TPM e pelo sensor seguro, e a única coisa exposta durante a autenticação é o HMAC de curta duração.</span><span class="sxs-lookup"><span data-stu-id="c4286-114">Secrets are held by the TPM and the secure sensor, and the only thing that is exposed during the authentication is the short-lived HMAC.</span></span>

## <a name="secure-sensor-capability"></a><span data-ttu-id="c4286-115">Capacidade de sensor seguro</span><span class="sxs-lookup"><span data-stu-id="c4286-115">Secure sensor capability</span></span>

<span data-ttu-id="c4286-116">O \_ recurso de sensor seguro de capacidade de WINBIO \_ \_ deve ser relatado pelo sensor se ele der suporte aos novos métodos de adaptador de mecanismo em v 4,0 da interface do adaptador do mecanismo.</span><span class="sxs-lookup"><span data-stu-id="c4286-116">The WINBIO\_CAPABILITY\_SECURE\_SENSOR capability must be reported by the sensor if it supports the new engine adapter methods in v 4.0 of the engine adapter interface.</span></span>

<span data-ttu-id="c4286-117">Para declarar que um sensor é um sensor seguro, ele deve atender aos seguintes requisitos:</span><span class="sxs-lookup"><span data-stu-id="c4286-117">To claim that a sensor is a secure sensor it must meet the following requirements:</span></span>

-   <span data-ttu-id="c4286-118">O mecanismo de correspondência do sensor deve ser isolado do sistema operacional normal (por exemplo, usando um ambiente de execução confiável)</span><span class="sxs-lookup"><span data-stu-id="c4286-118">The matching engine of the sensor must be isolated from the normal OS (for example, using a trusted execution environment)</span></span>
-   <span data-ttu-id="c4286-119">O sensor deve dar suporte à entrada segura de amostras para o mecanismo de correspondência isolado; o conteúdo dos exemplos nunca deve ser exposto ao sistema operacional normal</span><span class="sxs-lookup"><span data-stu-id="c4286-119">The sensor must support secure input of samples to the isolated matching engine; the content of the samples must never be exposed to the normal OS</span></span>
-   <span data-ttu-id="c4286-120">O mecanismo de correspondência deve dar suporte à versão de credencial segura implementando os novos métodos v4 descritos abaixo</span><span class="sxs-lookup"><span data-stu-id="c4286-120">The matching engine must support secure credential release by implementing the new v4 methods outlined below</span></span>
-   <span data-ttu-id="c4286-121">O sensor deve dar suporte à detecção de ataque de apresentação.</span><span class="sxs-lookup"><span data-stu-id="c4286-121">The sensor must support presentation attack detection.</span></span>

<span data-ttu-id="c4286-122">O \_ valor do \_ sensor seguro do recurso WINBIO \_ está contido na estrutura de [**\_ recursos do WINBIO**](/windows-hardware/drivers/ddi/winbio_ioctl/ns-winbio_ioctl-_winbio_sensor_attributes) .</span><span class="sxs-lookup"><span data-stu-id="c4286-122">The WINBIO\_CAPABILITY\_SECURE\_SENSOR value is contained in the [**WINBIO\_CAPABILITIES**](/windows-hardware/drivers/ddi/winbio_ioctl/ns-winbio_ioctl-_winbio_sensor_attributes) structure.</span></span> <span data-ttu-id="c4286-123">Aqui está um exemplo de como defini-lo.</span><span class="sxs-lookup"><span data-stu-id="c4286-123">Here's an example of how to define it.</span></span>


```
#define WINBIO_CAPABILITY_SECURE_SENSOR     ((WINBIO_CAPABILITIES)0x00000100)
```



## <a name="error-codes"></a><span data-ttu-id="c4286-124">Códigos de erro</span><span class="sxs-lookup"><span data-stu-id="c4286-124">Error Codes</span></span>


```C++
//
// MessageId: WINBIO_E_INVALID_KEY_IDENTIFIER
//
// MessageText:
//
// The key identifier is invalid.
//
#define WINBIO_E_INVALID_KEY_IDENTIFIER ((HRESULT)0x80098052L)

//
// MessageId: WINBIO_E_KEY_CREATION_FAILED
//
// MessageText:
//
// The key cannot be created.
//
#define WINBIO_E_KEY_CREATION_FAILED ((HRESULT)0x80098053L)

// 
// MessageId: WINBIO_E_KEY_IDENTIFIER_BUFFER_TOO_SMALL 
//
// MessageText: 
// 
// The key identifier buffer is too small. 
// 
#define WINBIO_E_KEY_IDENTIFIER_BUFFER_TOO_SMALL ((HRESULT)0x80098054L)
```



## <a name="engine-adapter-interface-v-40"></a><span data-ttu-id="c4286-125">Interface do adaptador do mecanismo v 4,0</span><span class="sxs-lookup"><span data-stu-id="c4286-125">Engine adapter interface v 4.0</span></span>

<span data-ttu-id="c4286-126">A versão da interface do adaptador do mecanismo foi incrementada para 4,0.</span><span class="sxs-lookup"><span data-stu-id="c4286-126">The engine adapter interface version has been incremented to 4.0.</span></span> <span data-ttu-id="c4286-127">As funções adicionais na nova interface permitem que o sensor participe do TPM 2,0.</span><span class="sxs-lookup"><span data-stu-id="c4286-127">The additional functions in the new interface allow the sensor to participate in TPM 2.0.</span></span> <span data-ttu-id="c4286-128">Eles são:</span><span class="sxs-lookup"><span data-stu-id="c4286-128">They are:</span></span>

-   [<span data-ttu-id="c4286-129">**EngineAdapterCreateKey**</span><span class="sxs-lookup"><span data-stu-id="c4286-129">**EngineAdapterCreateKey**</span></span>](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_create_key_fn)
-   [<span data-ttu-id="c4286-130">**EngineAdapterIdentifyFeatureSetSecure**</span><span class="sxs-lookup"><span data-stu-id="c4286-130">**EngineAdapterIdentifyFeatureSetSecure**</span></span>](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_feature_set_secure_fn)


```
// 

// Additional methods available in V4.0 and later 

// 


typedef HRESULT 

(WINAPI *PIBIO_ENGINE_CREATE_KEY_FN)( 

    _Inout_ PWINBIO_PIPELINE Pipeline, 

    _In_reads_(KeySize) const UCHAR* Key, 

    _In_ SIZE_T KeySize, 

    _Out_writes_bytes_to_(KeyIdentifierSize, *ResultSize) PUCHAR KeyIdentifier, 

    _In_ SIZE_T KeyIdentifierSize, 

    _Out_ PSIZE_T ResultSize 

    ); 


typedef HRESULT 

(WINAPI *PIBIO_ENGINE_IDENTIFY_FEATURE_SET_SECURE_FN)( 

    _Inout_ PWINBIO_PIPELINE Pipeline, 

    _In_reads_(NonceSize) const UCHAR* Nonce, 

    _In_ SIZE_T NonceSize, 

    _In_reads_(KeyIdentifierSize) const UCHAR* KeyIdentifier, 

    _In_ SIZE_T KeyIdentifierSize, 

    _Out_ PWINBIO_IDENTITY Identity, 

    _Out_ PWINBIO_BIOMETRIC_SUBTYPE SubFactor, 

 _Out_ PWINBIO_REJECT_DETAIL RejectDetail, 

    _Outptr_result_bytebuffer_(*AuthorizationSize) PUCHAR *Authorization, 

    _Out_ PSIZE_T AuthorizationSize 

    ); 


#define WINBIO_ENGINE_INTERFACE_VERSION_4   WINBIO_MAKE_INTERFACE_VERSION(4,0) 


typedef struct _WINBIO_ENGINE_INTERFACE { 

    WINBIO_ADAPTER_INTERFACE_VERSION            Version; 

    WINBIO_ADAPTER_TYPE                         Type; 

    SIZE_T                                      Size; 

    GUID                                        AdapterId; 


    PIBIO_ENGINE_ATTACH_FN                      Attach; 

    PIBIO_ENGINE_DETACH_FN                      Detach; 


    PIBIO_ENGINE_CLEAR_CONTEXT_FN               ClearContext; 


    PIBIO_ENGINE_QUERY_PREFERRED_FORMAT_FN      QueryPreferredFormat; 

    PIBIO_ENGINE_QUERY_INDEX_VECTOR_SIZE_FN     QueryIndexVectorSize; 

    PIBIO_ENGINE_QUERY_HASH_ALGORITHMS_FN       QueryHashAlgorithms; 

    PIBIO_ENGINE_SET_HASH_ALGORITHM_FN          SetHashAlgorithm; 


    PIBIO_ENGINE_QUERY_SAMPLE_HINT_FN           QuerySampleHint; 


    PIBIO_ENGINE_ACCEPT_SAMPLE_DATA_FN          AcceptSampleData;       // PROCESSES CURRENT BUFFER FROM PIPELINE AND GENERATES A FEATURE SET IN THE PIPELINE 

    PIBIO_ENGINE_EXPORT_ENGINE_DATA_FN          ExportEngineData;       // EXPORTS FEATURE SET OR TEMPLATE 


    PIBIO_ENGINE_VERIFY_FEATURE_SET_FN          VerifyFeatureSet; 

    PIBIO_ENGINE_IDENTIFY_FEATURE_SET_FN        IdentifyFeatureSet; 


    PIBIO_ENGINE_CREATE_ENROLLMENT_FN           CreateEnrollment;       // ATTACHES AN EMPTY ENROLLMENT TEMPLATE TO THE PIPELINE 

    PIBIO_ENGINE_UPDATE_ENROLLMENT_FN           UpdateEnrollment;       // CONVERTS CURRENT PIPELINE FEATURE SET INTO SOMETHING THAT CAN BE ADDED TO A TEMPLATE 

    PIBIO_ENGINE_GET_ENROLLMENT_STATUS_FN       GetEnrollmentStatus;    // QUERIES TEMPLATE ATTACHED TO THE PIPELINE TO SEE IF IT IS READY TO COMMIT 

    PIBIO_ENGINE_GET_ENROLLMENT_HASH_FN         GetEnrollmentHash; 

    PIBIO_ENGINE_CHECK_FOR_DUPLICATE_FN         CheckForDuplicate;      // DETERMINES WHETHER TEMPLATE IS ALREADY ENROLLED 

    PIBIO_ENGINE_COMMIT_ENROLLMENT_FN           CommitEnrollment; 

    PIBIO_ENGINE_DISCARD_ENROLLMENT_FN          DiscardEnrollment; 


    PIBIO_ENGINE_CONTROL_UNIT_FN                ControlUnit; 

    PIBIO_ENGINE_CONTROL_UNIT_PRIVILEGED_FN     ControlUnitPrivileged; 


#if (NTDDI_VERSION >= NTDDI_WIN8) 

    // 

    // V2.0 methods begin here... 

    // 

    PIBIO_ENGINE_NOTIFY_POWER_CHANGE_FN         NotifyPowerChange; 

    PIBIO_ENGINE_RESERVED_1_FN                  Reserved_1; 

#endif 


#if (NTDDI_VERSION >= NTDDI_WINTHRESHOLD) 

    // 

    // V3.0 methods begin here... 

    // 

    PIBIO_ENGINE_PIPELINE_INIT_FN                       PipelineInit; 

    PIBIO_ENGINE_PIPELINE_CLEANUP_FN                    PipelineCleanup; 

    PIBIO_ENGINE_ACTIVATE_FN                            Activate; 

    PIBIO_ENGINE_DEACTIVATE_FN                          Deactivate; 

    PIBIO_ENGINE_QUERY_EXTENDED_INFO_FN                 QueryExtendedInfo; 

    PIBIO_ENGINE_IDENTIFY_ALL_FN                        IdentifyAll; 

    PIBIO_ENGINE_SET_ENROLLMENT_SELECTOR_FN             SetEnrollmentSelector; 

    PIBIO_ENGINE_SET_ENROLLMENT_PARAMETERS_FN           SetEnrollmentParameters; 

    PIBIO_ENGINE_QUERY_EXTENDED_ENROLLMENT_STATUS_FN    QueryExtendedEnrollmentStatus; 

    PIBIO_ENGINE_REFRESH_CACHE_FN                       RefreshCache;  

    PIBIO_ENGINE_SELECT_CALIBRATION_FORMAT_FN           SelectCalibrationFormat; 

    PIBIO_ENGINE_QUERY_CALIBRATION_DATA_FN              QueryCalibrationData; 

    PIBIO_ENGINE_SET_ACCOUNT_POLICY_FN                  SetAccountPolicy; 

#endif 


#if (NTDDI_VERSION >= NTDDI_WIN10_RS1) 

    // 

    // V4.0 methods begin here... 

    // 

    PIBIO_ENGINE_CREATE_KEY_FN                     CreateKey; 

    PIBIO_ENGINE_IDENTIFY_FEATURE_SET_SECURE_FN    IdentifyFeatureSetSecure; 

#endif 


} WINBIO_ENGINE_INTERFACE, *PWINBIO_ENGINE_INTERFACE; 
```



## <a name="requirements"></a><span data-ttu-id="c4286-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4286-131">Requirements</span></span>

<span data-ttu-id="c4286-132">Windows 10</span><span class="sxs-lookup"><span data-stu-id="c4286-132">Windows 10</span></span>

 

 